---
title: 'Procédure : créer une paire de clés publique/privée'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- key pairs for strong-named assemblies
- signing assemblies
- assemblies [.NET Framework], signing
- cryptographic key pairs
- snk files (key pair files)
- public-private key pairs
- .snk files
- strong-named assemblies, key pairs
ms.assetid: 05026813-f3bd-4d7c-9e0b-fc588eb3d114
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 71eaaa85b8bd287c37f59116e75cf99b030d63ac
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59297835"
---
# <a name="how-to-create-a-public-private-key-pair"></a>Procédure : créer une paire de clés publique/privée

Pour signer un assembly avec un nom fort, vous devez disposer d’une paire de clés publique/privée. Cette paire de clés de chiffrement public et privé est utilisée lors de la compilation pour créer un assembly avec nom fort. Vous pouvez créer une paire de clés à l’aide de l’[outil Strong Name (Sn.exe)](../../../docs/framework/tools/sn-exe-strong-name-tool.md). Les fichiers de paire de clés ont généralement une extension .snk.

> [!NOTE]
> Dans Visual Studio, les pages de propriétés de projet C# et Visual Basic présentent un onglet **Signature** qui vous permet de sélectionner les fichiers de clé existants ou de générer de nouveaux fichiers de clé sans utiliser Sn.exe. Dans Visual C++, vous pouvez spécifier l’emplacement d’un fichier de clés existant dans la page de propriétés **Avancé** de la section **Éditeur de liens**, dans la section **Propriétés de Configuration** de la fenêtre **Pages de propriétés**. L’utilisation de l’attribut <xref:System.Reflection.AssemblyKeyFileAttribute> pour identifier les paires de fichiers de clés est devenue obsolète à partir de Visual Studio 2005.

## <a name="to-create-a-key-pair"></a>Pour créer une paire de clés

1. À l'invite de commandes, tapez la commande suivante :

     **sn –k** \<*nom de fichier*>

     Dans cette commande, *nom de fichier* est le nom du fichier de sortie contenant la paire de clés.

 L’exemple suivant crée une paire de clés appelée `sgKey.snk`.

```
sn -k sgKey.snk
```

 Si vous avez l’intention de temporiser la signature d’un assembly et que vous contrôlez la paire de clés entière (ce qui est improbable en dehors des scénarios de test), vous pouvez utiliser les commandes suivantes pour générer une paire de clés et ensuite en extraire la clé publique dans un fichier distinct. Commencez par créer la paire de clés :

```
sn -k keypair.snk
```

 Procédez ensuite à l’extraction de la clé publique de la paire de clés et copiez-la dans un fichier distinct :

```
sn -p keypair.snk public.snk
```

 Une fois que vous avez créé la paire de clés, vous devez placer le fichier à l’endroit où les outils de signature de nom fort peuvent le trouver.

 Lorsque vous signez un assembly avec un nom fort, l’utilitaire [Assembly Linker (Al.exe)](../../../docs/framework/tools/al-exe-assembly-linker.md) recherche le fichier de clés par rapport au répertoire en cours et au répertoire de sortie. Lorsque vous utilisez des compilateurs de ligne de commande, vous pouvez vous contenter de copier la clé dans le répertoire en cours contenant vos modules de code.

 Si vous utilisez une version antérieure de Visual Studio qui ne dispose pas d’onglet **Signature** dans les propriétés du projet, l’emplacement du fichier de clés recommandé est le répertoire du projet avec l’attribut de fichier spécifié comme suit :

 [!code-cpp[AssemblyName_KeyPair#21](../../../samples/snippets/cpp/VS_Snippets_CLR/AssemblyName_KeyPair/CPP/keyfileattrib.cpp#21)]
 [!code-csharp[AssemblyName_KeyPair#21](../../../samples/snippets/csharp/VS_Snippets_CLR/AssemblyName_KeyPair/CS/keyfileattrib.cs#21)]
 [!code-vb[AssemblyName_KeyPair#21](../../../samples/snippets/visualbasic/VS_Snippets_CLR/AssemblyName_KeyPair/VB/keyfileattrib.vb#21)]

## <a name="see-also"></a>Voir aussi

- [Création et utilisation d'assemblys avec nom fort](../../../docs/framework/app-domains/create-and-use-strong-named-assemblies.md)
