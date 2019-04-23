---
title: Les analyseurs de Roslyn - .NET
description: En savoir plus sur les analyseurs de Roslyn capables de détecter les problèmes et de suggérer des correctifs pour les résoudre.
author: billwagner
ms.author: wiwagn
ms.date: 01/24/2018
ms.technology: dotnet-standard
ms.openlocfilehash: 436cfb3904f0891f8c18bb5890563a13d65e2d1c
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62003052"
---
# <a name="the-roslyn-based-analyzers"></a>Les analyseurs de Roslyn

Les analyseurs de Roslyn utilisent le Kit de développement logiciel du compilateur .NET (API Roslyn) pour analyser le code source de votre projet pour détecter les problèmes et suggérer des corrections. Différents analyseurs recherchent différentes classes de problèmes, allant des pratiques susceptibles de provoquer des bogues à des problèmes de sécurité liés à la compatibilité avec les API.

Les analyseurs de Roslyn fonctionnent à la fois et de manière interactive pendant les builds. L’analyseur guide de différentes façons dans Visual Studio ou dans les builds de ligne de commande.

Lorsque vous modifiez le code dans Visual Studio, les analyseurs s’exécutent au moment de l’apport des modifications, interceptant d’éventuels problèmes dès que vous créez le code qui déclenche des problèmes. Les problèmes sont mis en surbrillance avec des tildes en-dessous. Visual Studio affiche une ampoule et lorsque vous cliquez dessus l’analyseur propose des solutions possibles à ce problème. Lorsque vous générez le projet, dans Visual Studio ou à partir de la ligne de commande, tout le code source est analysé et l’analyseur fournit une liste complète des problèmes potentiels. La figure suivante illustre un exemple.

![problèmes signalés par l’analyseur d’infrastructure](./media/framework-analyzers-2.png)

Les analyseurs de roslyn signalent des problèmes potentiels sous forme d’erreurs, d’avertissements ou d’informations en fonction de la gravité du problème.

Vous installez des analyseurs de Roslyn sous forme de packages NuGet dans votre projet. Les analyseurs configurés et tous les paramètres de chaque analyseur sont restaurés et s’exécutent sur l’ordinateur d’un développeur pour ce projet.

> [!NOTE]
> L’expérience utilisateur des analyseurs de Roslyn est différente de celle pour les bibliothèques d’analyse du code telles que les versions plus anciennes de FxCop et les outils d’analyse de sécurité.  Vous n’avez pas besoin exécuter explicitement les analyseurs de Roslyn. Il est inutile d’utiliser les éléments de menu « Exécuter l’analyse du code » dans le menu « Analyser » de Visual Studio. Les analyseurs de Roslyn s’exécutent de façon asynchrone lorsque vous travaillez.

## <a name="more-information-on-specific-analyzers"></a>En savoir plus sur les analyseurs spécifiques

Les analyseurs suivants sont couverts dans la présente section :

* [Analyseur d’API](api-analyzer.md) : Cet analyseur examine votre code à la recherche de risques potentiels de compatibilité ou d’utilisations d’API dépréciées.
* [Analyseur de framework](framework-analyzer.md) : Cet outil examine votre code pour s’assurer qu’il suit les instructions pour les applications .NET Framework. Ces règles incluent plusieurs recommandations de sécurité.
* [Analyseur de portabilité .NET](portability-analyzer.md) : Cet analyseur examine votre code afin de déterminer la quantité de travail nécessaire pour rendre votre application compatible avec d’autres profils et implémentations .NET, notamment .NET Core, .NET Standard, UWP et Xamarin pour iOS, Android et Mac.
