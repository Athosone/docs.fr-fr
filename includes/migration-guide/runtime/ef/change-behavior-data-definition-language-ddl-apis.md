---
ms.openlocfilehash: 1f06a185939c40274adad1ceac6990719069167a
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59235326"
---
### <a name="change-in-behavior-in-data-definition-language-ddl-apis"></a>Changement de comportement des API DDL (Data Definition Language)

|   |   |
|---|---|
|Détails|Le comportement des API DDL lors de la spécification d’AttachDBFilename a été modifié de la manière suivante :<ul><li>Les chaînes de connexion n’ont pas besoin de spécifier de valeur Initial Catalog. Avant, AttachDBFilename et Initial Catalog étaient obligatoires.</li><li>Si AttachDBFilename et Initial Catalog sont spécifiés et que le fichier MDF donné existe, la méthode <xref:System.Data.Objects.ObjectContext.DatabaseExists%2A> retourne <code>true</code>. Auparavant, elle retournait <code>false</code>.</li><li>Si AttachDBFilename et Initial Catalog sont spécifiés et que le fichier MDF donné existe, l’appel de la méthode <xref:System.Data.Objects.ObjectContext.DeleteDatabase%2A> a pour effet de supprimer les fichiers.</li><li>Si la méthode <xref:System.Data.Objects.ObjectContext.DeleteDatabase%2A> est appelée quand la chaîne de connexion spécifie une valeur AttachDBFilename avec un MDF et un catalogue initial qui n’existent pas, la méthode lève une exception <xref:System.InvalidOperationException>. Auparavant, elle levait une exception <xref:System.Data.SqlClient.SqlException>.</li></ul>|
|Suggestion|Ces modifications facilitent la création d'outils et d'applications qui utilisent les API DDL. Elles peuvent avoir une incidence sur la compatibilité des applications dans les scénarios suivants :<ul><li>L'utilisateur rédige du code qui exécute une commande <code>DROP DATABASE</code> directement au lieu d'appeler <xref:System.Data.Objects.ObjectContext.DeleteDatabase%2A> si <xref:System.Data.Objects.ObjectContext.DatabaseExists%2A> retourne <code>true</code>. Ce comportement altère le code existant si la base de données n'est pas liée mais que le fichier MDF existe.</li><li>L’utilisateur rédige du code qui attend de la méthode <xref:System.Data.Objects.ObjectContext.DeleteDatabase%2A> qu’elle lève une exception <xref:System.Data.SqlClient.SqlException> plutôt qu’une exception <xref:System.InvalidOperationException> quand le catalogue initial et le fichier MDF n’existent pas.</li></ul>|
|Portée|Mineur|
|Version|4.5|
|Type|Runtime|
