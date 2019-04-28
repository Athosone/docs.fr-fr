---
title: 'Procédure : configurer un service WCF hébergé par IIS avec SSL'
ms.date: 03/30/2017
ms.assetid: df2fe31f-a4bb-4024-92ca-b74ba055e038
ms.openlocfilehash: 8d3bbb1ceab8a3bc7e5e209fda29fd574110b4f7
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61699998"
---
# <a name="how-to-configure-an-iis-hosted-wcf-service-with-ssl"></a><span data-ttu-id="8203d-102">Procédure : configurer un service WCF hébergé par IIS avec SSL</span><span class="sxs-lookup"><span data-stu-id="8203d-102">How to: Configure an IIS-hosted WCF service with SSL</span></span>
<span data-ttu-id="8203d-103">Cette rubrique décrit comment installer un service WCF hébergé par IIS pour utiliser la sécurité de transport HTTP.</span><span class="sxs-lookup"><span data-stu-id="8203d-103">This topic describes how to set up an IIS-hosted WCF service to use HTTP transport security.</span></span> <span data-ttu-id="8203d-104">La sécurité de transport HTTP requiert un certificat SSL à enregistrer avec IIS.</span><span class="sxs-lookup"><span data-stu-id="8203d-104">HTTP transport security requires an SSL certificate to be registered with IIS.</span></span> <span data-ttu-id="8203d-105">Si vous n’avez pas de certificat SSL, vous pouvez utiliser IIS pour générer un certificat de test.</span><span class="sxs-lookup"><span data-stu-id="8203d-105">If you do not have an SSL certificate you can use IIS to generate a test certificate.</span></span> <span data-ttu-id="8203d-106">Vous devez ensuite ajouter une liaison SSL au site web et configurer les propriétés d’authentification du site web.</span><span class="sxs-lookup"><span data-stu-id="8203d-106">Next you must add an SSL binding to the web site and configure the web site’s authentication properties.</span></span> <span data-ttu-id="8203d-107">Enfin, vous devez configurer le service WCF pour utiliser HTTPS.</span><span class="sxs-lookup"><span data-stu-id="8203d-107">Finally you need to configure the WCF service to use HTTPS.</span></span>  
  
### <a name="creating-a-self-signed-certificate"></a><span data-ttu-id="8203d-108">Création d'un certificat auto-signé</span><span class="sxs-lookup"><span data-stu-id="8203d-108">Creating a Self-Signed Certificate</span></span>  
  
1. <span data-ttu-id="8203d-109">Ouvrez le Gestionnaire des services IIS (inetmgr.exe), puis choisissez le nom de votre ordinateur dans l’arborescence à gauche.</span><span class="sxs-lookup"><span data-stu-id="8203d-109">Open Internet Information Services Manager (inetmgr.exe), and select your computer name in the left-hand tree view.</span></span> <span data-ttu-id="8203d-110">Du côté droit de l'écran, sélectionnez Certificats de serveur.</span><span class="sxs-lookup"><span data-stu-id="8203d-110">On the right-hand side of the screen select Server Certificates</span></span>  
  
     <span data-ttu-id="8203d-111">![Écran d’accueil IIS Manager](../../../../docs/framework/wcf/feature-details/media/mg-inetmgrhome.jpg "mg_INetMgrHome")</span><span class="sxs-lookup"><span data-stu-id="8203d-111">![IIS Manager Home Screen](../../../../docs/framework/wcf/feature-details/media/mg-inetmgrhome.jpg "mg_INetMgrHome")</span></span>  
  
2. <span data-ttu-id="8203d-112">Dans la fenêtre certificats de serveur, cliquez sur le **créer un certificat auto-signé...**</span><span class="sxs-lookup"><span data-stu-id="8203d-112">In the Server Certificates window click the **Create Self-Signed Certificate….**</span></span> <span data-ttu-id="8203d-113">Lien.</span><span class="sxs-lookup"><span data-stu-id="8203d-113">Link.</span></span>  
  
     <span data-ttu-id="8203d-114">![Création d’un libre-service&#45;signé le certificat avec IIS](../../../../docs/framework/wcf/feature-details/media/mg-createselfsignedcert.jpg "mg_CreateSelfSignedCert")</span><span class="sxs-lookup"><span data-stu-id="8203d-114">![Creating a self&#45;signed certificate with IIS](../../../../docs/framework/wcf/feature-details/media/mg-createselfsignedcert.jpg "mg_CreateSelfSignedCert")</span></span>  
  
3. <span data-ttu-id="8203d-115">Entrez un nom convivial pour le certificat auto-signé et cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="8203d-115">Enter a friendly name for the self-signed certificate and click **OK**.</span></span>  
  
     <span data-ttu-id="8203d-116">![Créer ses enregistrements&#45;boîte de dialogue certificat signé](../../../../docs/framework/wcf/feature-details/media/mg-mycert.jpg "mg_MyCert")</span><span class="sxs-lookup"><span data-stu-id="8203d-116">![Create Self&#45;Signed Certificate Dialog](../../../../docs/framework/wcf/feature-details/media/mg-mycert.jpg "mg_MyCert")</span></span>  
  
     <span data-ttu-id="8203d-117">Les détails du certificat auto-signé nouvellement créé sont maintenant affichés dans le **certificats de serveur** fenêtre.</span><span class="sxs-lookup"><span data-stu-id="8203d-117">The newly created self-signed certificate details are now shown in the **Server Certificates** window.</span></span>  
  
     <span data-ttu-id="8203d-118">![Fenêtre certificat de serveur](../../../../docs/framework/wcf/feature-details/media/mg-servercertificatewindow.jpg "mg_ServerCertificateWindow")</span><span class="sxs-lookup"><span data-stu-id="8203d-118">![Server Certificate Window](../../../../docs/framework/wcf/feature-details/media/mg-servercertificatewindow.jpg "mg_ServerCertificateWindow")</span></span>  
  
     <span data-ttu-id="8203d-119">Le certificat généré est installé dans le magasin d'Autorités de certification racines de confiance.</span><span class="sxs-lookup"><span data-stu-id="8203d-119">The generated certificate is installed in the Trusted Root Certification Authorities store.</span></span>  
  
### <a name="add-ssl-binding"></a><span data-ttu-id="8203d-120">Ajouter une liaison SSL</span><span class="sxs-lookup"><span data-stu-id="8203d-120">Add SSL Binding</span></span>  
  
1. <span data-ttu-id="8203d-121">Toujours dans le Gestionnaire des Services Internet, développez le **Sites** dossier, puis le **Site Web par défaut** dossier dans l’arborescence sur le côté gauche de l’écran.</span><span class="sxs-lookup"><span data-stu-id="8203d-121">Still in Internet Information Services Manager, expand the **Sites** folder and then the **Default Web Site** folder in the tree view on the left-hand side of the screen.</span></span>  
  
2. <span data-ttu-id="8203d-122">Cliquez sur le **liaisons...**</span><span class="sxs-lookup"><span data-stu-id="8203d-122">Click the **Bindings….**</span></span> <span data-ttu-id="8203d-123">Lien dans le **Actions** section dans la partie supérieure droite de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="8203d-123">Link in the **Actions** section in the upper right hand portion of the window.</span></span>  
  
     <span data-ttu-id="8203d-124">![Ajout d’une liaison SSL](../../../../docs/framework/wcf/feature-details/media/mg-addsslbinding.jpg "mg_AddSSLBinding")</span><span class="sxs-lookup"><span data-stu-id="8203d-124">![Adding an SSL binding](../../../../docs/framework/wcf/feature-details/media/mg-addsslbinding.jpg "mg_AddSSLBinding")</span></span>  
  
3. <span data-ttu-id="8203d-125">Dans la fenêtre liaisons de Site, cliquez sur le **ajouter** bouton.</span><span class="sxs-lookup"><span data-stu-id="8203d-125">In the Site Bindings window click the **Add** button.</span></span>  
  
     <span data-ttu-id="8203d-126">![Boîte de dialogue liaisons de site](../../../../docs/framework/wcf/feature-details/media/mg-sitebindingsdialog.jpg "mg_SiteBindingsDialog")</span><span class="sxs-lookup"><span data-stu-id="8203d-126">![Site Bindings Dialog](../../../../docs/framework/wcf/feature-details/media/mg-sitebindingsdialog.jpg "mg_SiteBindingsDialog")</span></span>  
  
4. <span data-ttu-id="8203d-127">Dans le **ajouter la liaison de Site** boîte de dialogue, sélectionnez le protocole https pour le type et le nom convivial du certificat auto-signé que vous avez créé.</span><span class="sxs-lookup"><span data-stu-id="8203d-127">In the **Add Site Binding** dialog, select https for the type and the friendly name of the self-signed certificate you just created.</span></span>  
  
     <span data-ttu-id="8203d-128">![Exemple de liaison de site](../../../../docs/framework/wcf/feature-details/media/mg-mycertbinding.jpg "mg_MyCertBinding")</span><span class="sxs-lookup"><span data-stu-id="8203d-128">![Site binding example](../../../../docs/framework/wcf/feature-details/media/mg-mycertbinding.jpg "mg_MyCertBinding")</span></span>  
  
### <a name="configure-virtual-directory-for-ssl"></a><span data-ttu-id="8203d-129">Configurer le répertoire virtuel pour SSL</span><span class="sxs-lookup"><span data-stu-id="8203d-129">Configure Virtual Directory for SSL</span></span>  
  
1. <span data-ttu-id="8203d-130">Toujours dans le Gestionnaire des services IIS, sélectionnez le répertoire virtuel qui contient votre service sécurisé WCF.</span><span class="sxs-lookup"><span data-stu-id="8203d-130">Still in Internet Information Services Manager, select the virtual directory that contains your WCF secure service.</span></span>  
  
2. <span data-ttu-id="8203d-131">Dans le volet central de la fenêtre, sélectionnez **paramètres SSL** dans la section IIS.</span><span class="sxs-lookup"><span data-stu-id="8203d-131">In the center pane of the window, select **SSL Settings** in the IIS section.</span></span>  
  
     <span data-ttu-id="8203d-132">![Paramètres SSL pour le répertoire virtuel](../../../../docs/framework/wcf/feature-details/media/mg-sslsettingsforvdir.jpg "mg_SSLSettingsForVDir")</span><span class="sxs-lookup"><span data-stu-id="8203d-132">![SSL Settings for virtual directory](../../../../docs/framework/wcf/feature-details/media/mg-sslsettingsforvdir.jpg "mg_SSLSettingsForVDir")</span></span>  
  
3. <span data-ttu-id="8203d-133">Dans le volet Paramètres SSL, sélectionnez le **exiger SSL** case à cocher et cliquez sur le **appliquer** lien dans le **Actions** section sur le côté droit de l’écran.</span><span class="sxs-lookup"><span data-stu-id="8203d-133">In the SSL Settings pane, select the **Require SSL** checkbox and click the **Apply** link in the **Actions** section on the right hand side of the screen.</span></span>  
  
     <span data-ttu-id="8203d-134">![Paramètres de répertoire virtuel SSL](../../../../docs/framework/wcf/feature-details/media/mg-vdirsslsettings.JPG "mg_VDirSSLSettings")</span><span class="sxs-lookup"><span data-stu-id="8203d-134">![Virtual directory SSL settings](../../../../docs/framework/wcf/feature-details/media/mg-vdirsslsettings.JPG "mg_VDirSSLSettings")</span></span>  
  
### <a name="configure-wcf-service-for-http-transport-security"></a><span data-ttu-id="8203d-135">Configurer le service WCF pour la sécurité de transport HTTP</span><span class="sxs-lookup"><span data-stu-id="8203d-135">Configure WCF Service for HTTP Transport Security</span></span>  
  
1. <span data-ttu-id="8203d-136">Dans le fichier web.config du service WCF, configurez la liaison HTTP pour utiliser la sécurité de transport, comme indiqué dans le code XML suivant.</span><span class="sxs-lookup"><span data-stu-id="8203d-136">In the WCF service’s web.config configure the HTTP binding to use transport security as shown in the following XML.</span></span>  
  
    ```xml  
    <bindings>  
          <basicHttpBinding>  
            <binding name="secureHttpBinding">  
              <security mode="Transport">  
                <transport clientCredentialType="None"/>  
              </security>  
            </binding>  
          </basicHttpBinding>  
    </bindings>  
    ```  
  
2. <span data-ttu-id="8203d-137">Spécifiez votre service et point de terminaison de service comme indiqué dans le code XML suivant.</span><span class="sxs-lookup"><span data-stu-id="8203d-137">Specify your service and service endpoint as shown in the following XML.</span></span>  
  
    ```xml  
    <services>  
          <service name="MySecureWCFService.Service1">  
            <endpoint address=""  
                      binding="basicHttpBinding"  
                      bindingConfiguration="secureHttpBinding"  
                      contract="MySecureWCFService.IService1"/>  
  
            <endpoint address="mex"  
                      binding="mexHttpsBinding"  
                      contract="IMetadataExchange" />  
          </service>  
    </services>  
    ```  
  
## <a name="example"></a><span data-ttu-id="8203d-138">Exemple</span><span class="sxs-lookup"><span data-stu-id="8203d-138">Example</span></span>  
 <span data-ttu-id="8203d-139">Voici un exemple complet d'un fichier web.config pour un service WCF utilisant la sécurité de transport HTTP.</span><span class="sxs-lookup"><span data-stu-id="8203d-139">The following is a complete example of a web.config file for a WCF service using HTTP transport security</span></span>  
  
```xml  
<?xml version="1.0"?>  
<configuration>  
  
  <system.web>  
    <compilation debug="true" targetFramework="4.0" />  
  </system.web>  
  <system.serviceModel>  
    <services>  
      <service name="MySecureWCFService.Service1">  
        <endpoint address=""  
                  binding="basicHttpBinding"  
                  bindingConfiguration="secureHttpBinding"  
                  contract="MySecureWCFService.IService1"/>  
  
        <endpoint address="mex"  
                  binding="mexHttpsBinding"  
                  contract="IMetadataExchange" />  
      </service>  
    </services>  
    <bindings>  
      <basicHttpBinding>  
        <binding name="secureHttpBinding">  
          <security mode="Transport">  
            <transport clientCredentialType="None"/>  
          </security>  
        </binding>  
      </basicHttpBinding>  
    </bindings>  
    <behaviors>  
      <serviceBehaviors>  
        <behavior>  
          <!-- To avoid disclosing metadata information, set the value below to false and remove the metadata endpoint above before deployment -->  
          <serviceMetadata httpsGetEnabled="true"/>  
          <!-- To receive exception details in faults for debugging purposes, set the value below to true.  Set to false before deployment to avoid disclosing exception information -->  
          <serviceDebug includeExceptionDetailInFaults="false"/>  
        </behavior>  
      </serviceBehaviors>  
    </behaviors>  
    <serviceHostingEnvironment multipleSiteBindingsEnabled="true" />  
  </system.serviceModel>  
  <system.webServer>  
    <modules runAllManagedModulesForAllRequests="true"/>  
  </system.webServer>  
  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="8203d-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8203d-140">See also</span></span>

- [<span data-ttu-id="8203d-141">Hébergement dans les services IIS (Internet Information Services)</span><span class="sxs-lookup"><span data-stu-id="8203d-141">Hosting in Internet Information Services</span></span>](../../../../docs/framework/wcf/feature-details/hosting-in-internet-information-services.md)
- [<span data-ttu-id="8203d-142">Instructions relatives à l’hébergement dans Internet Information Services</span><span class="sxs-lookup"><span data-stu-id="8203d-142">Internet Information Service Hosting Instructions</span></span>](../../../../docs/framework/wcf/samples/internet-information-service-hosting-instructions.md)
- [<span data-ttu-id="8203d-143">Bonnes pratiques pour l’hébergement dans Internet Information Services</span><span class="sxs-lookup"><span data-stu-id="8203d-143">Internet Information Services Hosting Best Practices</span></span>](../../../../docs/framework/wcf/feature-details/internet-information-services-hosting-best-practices.md)
- [<span data-ttu-id="8203d-144">Hébergement IIS à l’aide de code en ligne</span><span class="sxs-lookup"><span data-stu-id="8203d-144">IIS Hosting Using Inline Code</span></span>](../../../../docs/framework/wcf/samples/iis-hosting-using-inline-code.md)
