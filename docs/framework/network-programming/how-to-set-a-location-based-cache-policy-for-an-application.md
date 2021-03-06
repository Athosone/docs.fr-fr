---
title: 'Procédure : définir une stratégie de cache basée sur l’emplacement pour une application'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- expliciting defining cache behavior
- location-based cache policies
- local cache
- request cache policies
- cache [.NET Framework], location-based policies
ms.assetid: 683bb88e-3411-4f46-9686-3411b6ba511c
ms.openlocfilehash: 06d458828c77f61e03d18f635ec00f6a7267bab8
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59341866"
---
# <a name="how-to-set-a-location-based-cache-policy-for-an-application"></a>Procédure : définir une stratégie de cache basée sur l’emplacement pour une application
Avec une stratégie de cache basée sur l’emplacement, une application peut définir explicitement le comportement de cache en fonction de l’emplacement de la ressource demandée. Cette rubrique explique comment définir la stratégie de cache par programmation. Pour plus d’informations sur la définition de la stratégie pour une application en utilisant les fichiers de configuration, consultez [\<requestCaching>, élément (paramètres réseau)](../../../docs/framework/configure-apps/file-schema/network/requestcaching-element-network-settings.md).  
  
### <a name="to-set-a-location-based-cache-policy-for-an-application"></a>Pour définir une stratégie de cache basée sur l’emplacement pour une application  
  
1. Créez un objet <xref:System.Net.Cache.RequestCachePolicy> ou <xref:System.Net.Cache.HttpRequestCachePolicy>.  
  
2. Définissez l’objet de stratégie par défaut pour le domaine d’application.  
  
### <a name="to-set-a-policy-that-takes-requested-resources-from-a-cache"></a>Pour définir une stratégie qui obtient les ressources demandées à partir d’un cache  
  
-   Créez une stratégie qui obtient les ressources demandées à partir d’un cache disponible ou, sinon, qui envoie les demandes au serveur (pour cela, définissez le niveau de cache à <xref:System.Net.Cache.HttpRequestCacheLevel.CacheIfAvailable>). Une demande peut être traitée par n’importe quel cache entre le client et le serveur, y compris les caches distants.  
  
    ```csharp  
    public static void UseCacheIfAvailable()  
    {  
        HttpRequestCachePolicy policy = new HttpRequestCachePolicy  
            (HttpRequestCacheLevel.CacheIfAvailable);  
        HttpWebRequest.DefaultCachePolicy = policy;  
    }  
    ```  
  
    ```vb  
    Public Shared Sub UseCacheIfAvailable()  
        Dim policy As New HttpRequestCachePolicy _  
             (HttpRequestCacheLevel.CacheIfAvailable)  
        HttpWebRequest.DefaultCachePolicy = policy  
    End Sub  
    ```  
  
### <a name="to-set-a-policy-that-prevents-any-cache-from-supplying-resources"></a>Pour définir une stratégie qui empêche tous les caches de fournir des ressources  
  
-   Créez une stratégie qui empêche tous les caches de fournir les ressources demandées en définissant le niveau de cache à <xref:System.Net.Cache.HttpRequestCacheLevel.NoCacheNoStore>. Ce niveau de stratégie supprime la ressource qui se trouve éventuellement dans le cache local et spécifie que les caches distants doivent également supprimer cette ressource.  
  
    ```csharp  
    public static void DoNotUseCache()  
    {  
    HttpRequestCachePolicy policy = new HttpRequestCachePolicy   
            (HttpRequestCacheLevel.NoCacheNoStore);  
        HttpWebRequest.DefaultCachePolicy = policy;  
    }  
    ```  
  
    ```vb  
    Public Shared Sub DoNotUseCache()  
        Dim policy As New HttpRequestCachePolicy _  
            (HttpRequestCacheLevel.NoCacheNoStore)  
        HttpWebRequest.DefaultCachePolicy = policy  
    End Sub  
    ```  
  
### <a name="to-set-a-policy-that-returns-requested-resources-only-if-they-are-in-the-local-cache"></a>Pour définir une stratégie qui retourne les ressources demandées uniquement si elles sont dans le cache local  
  
-   Créez une stratégie qui retourne les ressources demandées uniquement si elles sont dans le cache local en définissant le niveau de cache à <xref:System.Net.Cache.HttpRequestCacheLevel.CacheOnly>. Si la ressource demandée n’est pas dans le cache, une exception <xref:System.Net.WebException> est levée.  
  
    ```csharp  
    public static void OnlyUseCache()  
    {  
        HttpRequestCachePolicy policy = new HttpRequestCachePolicy   
            (HttpRequestCacheLevel.CacheOnly);  
        HttpWebRequest.DefaultCachePolicy = policy;  
    }  
    ```  
  
    ```vb  
    Public Shared Sub OnlyUseCache()  
        Dim policy As New HttpRequestCachePolicy _  
            (HttpRequestCacheLevel.CacheOnly)  
        HttpWebRequest.DefaultCachePolicy = policy  
    End Sub  
    ```  
  
### <a name="to-set-a-policy-that-prevents-the-local-cache-from-supplying-resources"></a>Pour définir une stratégie qui empêche le cache local de fournir des ressources  
  
-   Créez une stratégie qui empêche le cache local de fournir les ressources demandées en définissant le niveau de cache à <xref:System.Net.Cache.HttpRequestCacheLevel.Refresh>. Si la ressource demandée se trouve dans un cache intermédiaire et qu’elle a été revalidée, le cache intermédiaire est autorisé à fournir cette ressource.  
  
    ```csharp  
    public static void DoNotUseLocalCache()  
    {  
     HttpRequestCachePolicy policy = new HttpRequestCachePolicy   
            (HttpRequestCacheLevel.Refresh);  
        HttpWebRequest.DefaultCachePolicy = policy;  
    }  
    ```  
  
    ```vb  
    Public Shared Sub DoNotUseLocalCache()  
        Dim policy As New HttpRequestCachePolicy _  
            (HttpRequestCacheLevel.Refresh)  
        HttpWebRequest.DefaultCachePolicy = policy  
    End Sub  
    ```  
  
### <a name="to-set-a-policy-that-prevents-any-cache-from-supplying-requested-resources"></a>Pour définir une stratégie qui empêche tous les caches de fournir les ressources demandées  
  
-   Créez une stratégie qui empêche tous les caches de fournir les ressources demandées en définissant le niveau de cache à <xref:System.Net.Cache.HttpRequestCacheLevel.Reload>. La ressource retournée par le serveur peut être stockée dans le cache.  
  
    ```csharp  
    public static void SendToServer()  
    {  
    HttpRequestCachePolicy policy = new HttpRequestCachePolicy   
            (HttpRequestCacheLevel.Reload);  
        HttpWebRequest.DefaultCachePolicy = policy;  
    }  
    ```  
  
    ```vb  
    Public Shared Sub SendToServer()  
        Dim policy As New HttpRequestCachePolicy _  
            (HttpRequestCacheLevel.Reload)  
        HttpWebRequest.DefaultCachePolicy = policy  
    End Sub  
    ```  
  
### <a name="to-set-a-policy-that-allows-any-cache-to-supply-requested-resources-if-the-resource-on-the-server-is-not-newer-than-the-cached-copy"></a>Pour définir une stratégie qui autorise tous les caches à fournir les ressources demandées si la ressource sur le serveur n’est pas plus récente que la copie en cache  
  
-   Créez une stratégie qui autorise tous les caches à fournir les ressources demandées si la ressource sur le serveur n’est pas plus récente que la copie en cache, en définissant le niveau de cache à <xref:System.Net.Cache.HttpRequestCacheLevel.Revalidate>.  
  
    ```csharp  
    public static void CheckServer()  
    {  
    HttpRequestCachePolicy policy = new HttpRequestCachePolicy  
             (HttpRequestCacheLevel.Revalidate);  
        HttpWebRequest.DefaultCachePolicy = policy;  
    }  
    ```  
  
    ```vb  
    Public Shared Sub CheckServer()  
        Dim policy As New HttpRequestCachePolicy _  
            (HttpRequestCacheLevel.Revalidate)  
        HttpWebRequest.DefaultCachePolicy = policy  
    End Sub  
    ```  
  
## <a name="see-also"></a>Voir aussi

- [Gestion du cache pour les applications réseau](../../../docs/framework/network-programming/cache-management-for-network-applications.md)
- [Stratégie de cache](../../../docs/framework/network-programming/cache-policy.md)
- [Stratégies de cache basées sur l’emplacement](../../../docs/framework/network-programming/location-based-cache-policies.md)
- [Stratégies de cache basées sur la durée](../../../docs/framework/network-programming/time-based-cache-policies.md)
- [\<requestCaching>, élément (paramètres réseau)](../../../docs/framework/configure-apps/file-schema/network/requestcaching-element-network-settings.md)
