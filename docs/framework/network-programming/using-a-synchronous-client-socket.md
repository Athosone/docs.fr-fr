---
title: Utilisation d’un socket client synchrone
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- application protocols, sockets
- sending data, sockets
- data requests, sockets
- requesting data from Internet, sockets
- synchronous client sockets
- Socket class, synchronous client sockets
- receiving data, sockets
- sockets, synchronous client sockets
- protocols, sockets
- Internet, sockets
- client sockets
ms.assetid: 945d00c6-7202-466c-9df9-140b84156d43
ms.openlocfilehash: 339f9c9d8b25f6deef4cc77f60c26b7b5d017ce0
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59105779"
---
# <a name="using-a-synchronous-client-socket"></a>Utilisation d’un socket client synchrone
Un socket client synchrone interrompt l’exécution de l’application durant l’opération réseau. Les sockets synchrones ne sont pas appropriés pour les applications dont l’exécution nécessite une utilisation intensive du réseau, mais ils facilitent l’accès aux services réseau pour les autres applications.  
  
 Pour envoyer les données, passez un tableau d’octets à l’une des méthodes d’envoi de données de la classe <xref:System.Net.Sockets.Socket> (<xref:System.Net.Sockets.Socket.Send%2A> et <xref:System.Net.Sockets.Socket.SendTo%2A>). L’exemple suivant encode une chaîne dans une mémoire tampon de tableau d’octets à l’aide de la propriété <xref:System.Text.Encoding.ASCII%2A?displayProperty=nameWithType>, puis transmet la mémoire tampon à l’appareil réseau avec la méthode **Send**. La méthode **Send** retourne le nombre d’octets envoyés à l’appareil réseau.  
  
```vb  
Dim msg As Byte() = _  
    System.Text.Encoding.ASCII.GetBytes("This is a test.")  
Dim bytesSent As Integer = s.Send(msg)  
```  
  
```csharp  
byte[] msg = System.Text.Encoding.ASCII.GetBytes("This is a test");  
int bytesSent = s.Send(msg);  
```  
  
 La méthode **Send** supprime les octets dans la mémoire tampon et les met en file d’attente dans l’interface réseau pour l’envoi à l’appareil réseau. L’interface réseau peut ne pas envoyer les données immédiatement, mais les envoyer plus tard, dès que la connexion sera fermée normalement avec la méthode <xref:System.Net.Sockets.Socket.Shutdown%2A>.  
  
 Pour recevoir les données d’un appareil réseau, passez une mémoire tampon à l’une des méthodes de réception de données de la classe **Socket** (<xref:System.Net.Sockets.Socket.Receive%2A> et <xref:System.Net.Sockets.Socket.ReceiveFrom%2A>). Les sockets synchrones interrompent l’exécution de l’application jusqu’à la réception des octets du réseau ou la fermeture du socket. L’exemple suivant reçoit les données du réseau, puis les affiche sur la console. L’exemple suppose que les données provenant du réseau sont encodées en texte ASCII. La méthode **Receive** retourne le nombre d’octets reçus du réseau.  
  
```vb  
Dim bytes(1024) As Byte  
Dim bytesRec = s.Receive(bytes)  
Console.WriteLine("Echoed text = {0}", _  
    System.Text.Encoding.ASCII.GetString(bytes, 0, bytesRec))  
```  
  
```csharp  
byte[] bytes = new byte[1024];  
int bytesRec = s.Receive(bytes);  
Console.WriteLine("Echoed text = {0}",  
    System.Text.Encoding.ASCII.GetString(bytes, 0, bytesRec));  
```  
  
 Quand le socket n’est plus nécessaire, vous devez le libérer en appelant la méthode <xref:System.Net.Sockets.Socket.Shutdown%2A>, puis la méthode **Close**. L’exemple suivant libère un **Socket**. L’énumération <xref:System.Net.Sockets.SocketShutdown> définit les constantes qui indiquent si le socket doit être fermé pour l’envoi et/ou la réception des données.  
  
```vb  
s.Shutdown(SocketShutdown.Both)  
s.Close()  
```  
  
```csharp  
s.Shutdown(SocketShutdown.Both);  
s.Close();  
```  
  
## <a name="see-also"></a>Voir aussi

- [Utilisation d’un socket client asynchrone](../../../docs/framework/network-programming/using-an-asynchronous-client-socket.md)
- [Écoute avec des sockets](../../../docs/framework/network-programming/listening-with-sockets.md)
- [Exemple de socket client synchrone](../../../docs/framework/network-programming/synchronous-client-socket-example.md)
