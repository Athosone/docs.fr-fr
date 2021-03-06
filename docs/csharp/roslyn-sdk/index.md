---
title: Kit SDK .NET Compiler Platform (API Roslyn)
description: Apprenez à utiliser le Kit de développement logiciel (SDK) .NET Compiler Platform (également appelé API Roslyn) pour comprendre le code .NET, identifier les erreurs et les corriger.
ms.date: 10/10/2017
ms.custom: mvc
ms.openlocfilehash: ea733d4c5c54c18e510a028f3a724f89490db9dd
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61706544"
---
# <a name="the-net-compiler-platform-sdk"></a>Kit SDK .NET Compiler Platform

Les compilateurs génèrent un modèle détaillé du code applicatif lorsqu’ils en valident la syntaxe et la sémantique. Ce modèle permet de générer la sortie exécutable à partir du code source. Le Kit SDK .NET Compiler Platform donne accès à ce modèle. Nous nous appuyons de plus en plus sur des fonctionnalités d’environnements de développement intégré (IDE) telles qu’IntelliSense, la refactorisation, le renommage intelligent, la recherche de l’ensemble des références et l’accès direct aux définitions pour augmenter notre productivité. Nous utilisons des outils d’analyse du code pour améliorer la qualité de notre code et des générateurs de code pour faciliter la construction des applications. Plus ces outils gagnent en intelligence, plus ils ont besoin d’accéder à une grande part du modèle que seuls les compilateurs créent lorsqu’ils traitent le code applicatif. Il s’agit de la mission centrale des API Roslyn : ouvrir les boîtes noires et laisser les outils et les utilisateurs finaux partager toute la richesse des informations que possèdent les compilateurs sur notre code.
Au lieu de rester d’opaques traducteurs de code source en code objet, les compilateurs deviennent des plateformes avec Roslyn : des API utilisables pour les tâches portant sur le code dans les outils et les applications souhaités.

## <a name="net-compiler-platform-sdk-concepts"></a>Concepts du Kit SDK .NET Compiler Platform

Le Kit SDK .NET Compiler Platform réduit considérablement la barrière à l’entrée pour la création d’applications et d’outils axés sur le code. Il offre de nombreuses possibilités d’innovation dans différents champs, notamment la métaprogrammation, la génération et la transformation de code, l’utilisation interactive des langages C# et VB et l’incorporation de C# et de VB dans des langages propres au domaine.

Le Kit SDK .NET Compiler Platform permet de générer des ***analyseurs*** et des ***correctifs de code*** qui recherchent et corrigent les erreurs de codage. Les ***analyseurs*** comprennent la syntaxe et la structure du code, et détectent les pratiques à corriger. Les ***correctifs de code*** représentent des propositions de correction des erreurs de codage trouvées par les analyseurs. En règle générale, un analyseur et les correctifs de code associés sont regroupés dans un seul projet.

Les analyseurs et les correctifs de code utilisent l’analyse statique pour comprendre le code. Ils n’exécutent pas le code, et n’offrent aucun autre avantage en matière de tests. Ils peuvent, toutefois, signaler des pratiques qui aboutissent souvent à des bogues, à du code empêchant toute mise à jour ou à la violation des recommandations standard.

Le Kit SDK .NET Compiler Platform se compose d’un unique ensemble d’API permettant d’examiner et de comprendre un codebase C# ou Visual Basic. Grâce à ce codebase unique, il est plus facile d’écrire des analyseurs et des correctifs de code en utilisant les API d’analyse syntaxique et sémantique fournies par le Kit SDK .NET Compiler Platform. Une fois libéré de la tâche chronophage qui consiste à répliquer l’analyse effectuée par le compilateur, vous pouvez vous concentrer sur la tâche, plus ciblée, de recherche et de résolution des erreurs de codage courantes de votre projet ou de votre bibliothèque.

Autre avantage, plus modeste, vos analyseurs et vos correctifs de code sont plus petits et utilisent beaucoup moins de mémoire une fois chargés dans Visual Studio que si vous aviez écrit votre propre codebase pour comprendre le code d’un projet. En exploitant les mêmes classes que le compilateur et Visual Studio, vous pouvez créer vos propres outils d’analyse statique. Votre équipe a donc la possibilité d’utiliser des analyseurs et des correctifs de code sans impact perceptible sur les performances de l’IDE.

Il existe trois grands scénarios d’écriture d’analyseurs et de correctifs de code :

1. [*Appliquer des normes de codage pour l’équipe*](#enforce-team-coding-standards)
1. [*Offrir de l’aide sur les packages de bibliothèque*](#provide-guidance-with-library-packages)
1. [*Proposer des conseils généraux*](#provide-general-guidance)

## <a name="enforce-team-coding-standards"></a>Appliquer des normes de codage pour l’équipe

De nombreuses équipes ont des normes de codage, qui sont appliquées par le biais des révisions du code effectuées avec d’autres membres de l’équipe. Les analyseurs et les correctifs de code peuvent rendre ce processus beaucoup plus efficace. Les revues de code se produisent quand un développeur partage son travail avec d’autres membres de l’équipe. Le développeur aura investi tout le temps nécessaire pour terminer une nouvelle fonctionnalité avant de recevoir le moindre commentaire. Plusieurs semaines peuvent s’écouler, au cours desquelles le développeur renforce des habitudes qui ne correspondent pas aux pratiques de l’équipe.

Les analyseurs s’exécutent au moment même où il écrit du code. Le développeur obtient immédiatement des commentaires qui l’encouragent à suivre les instructions sans attendre. Le développeur prend l’habitude d’écrire du code conforme dès qu’il commence le prototypage. Lorsque la fonctionnalité est prête à être révisée par des humains, toutes les instructions standard ont été appliquées.

Les équipes peuvent créer des analyseurs et des correctifs de code permettant de rechercher les pratiques les plus courantes qui enfreignent les pratiques de codage de l’équipe. Ils peuvent être installés sur l’ordinateur de chaque développeur pour appliquer les normes.

## <a name="provide-guidance-with-library-packages"></a>Offrir de l’aide sur les packages de bibliothèque

Il existe une multitude de bibliothèques accessibles aux développeurs .NET sur NuGet.
Certaines proviennent de Microsoft ou de sociétés tierces, d’autres sont proposées par des membres de la communauté et des bénévoles. Ces bibliothèques sont plus souvent utilisées et sont mieux notées lorsque les développeurs réussissent à les exploiter.

En plus de la documentation, vous pouvez proposer des analyseurs et des correctifs de code qui recherchent et corrigent les mauvais emplois courants de votre bibliothèque. Ces corrections immédiates aident les développeurs à en tirer parti plus rapidement.

Vous pouvez ajouter les analyseurs et les correctifs de code au package de votre bibliothèque sur NuGet. Dans ce scénario, un développeur qui installe votre package NuGet installera également le package de l’analyseur. Tous les développeurs qui utilisent votre bibliothèque obtiennent immédiatement de l’aide de la part de votre équipe sous la forme de commentaires immédiats sur les erreurs et de suggestions de corrections.

## <a name="provide-general-guidance"></a>Proposer des conseils généraux

La communauté de développeurs .NET a découvert, par l’expérience, des modèles qui fonctionnent bien et d’autres qu’il vaut mieux éviter. Plusieurs membres de la communauté ont créé des analyseurs qui appliquent ces modèles recommandés. Plus nous gagnons en expérience, plus il y a de place pour de nouvelles idées.

Ces analyseurs peuvent être chargés sur [Visual Studio Marketplace](https://marketplace.visualstudio.com/vs) et téléchargés par les développeurs avec Visual Studio. Ceux qui débutent avec le langage et la plateforme apprennent rapidement les pratiques acceptées et deviennent plus vite productifs, dès le début de leur parcours d’apprentissage de .NET. Comme ils sont de plus en plus utilisés, la communauté adopte ces pratiques.

## <a name="next-steps"></a>Étapes suivantes

Le Kit SDK .NET Compiler Platform inclut les derniers modèles objet du langage pour la génération, l’analyse et la refactorisation de code. Cette section offre une vue d’ensemble conceptuelle du Kit SDK .NET Compiler Platform. Vous trouverez plus de détails dans les sections des didacticiels, des exemples et des démarrages rapides.

Pour en savoir plus sur les concepts du Kit SDK .NET Compiler Platform, consultez ces cinq rubriques :

- [Explorer le code avec le visualiseur de syntaxe](syntax-visualizer.md)
- [Comprendre le modèle de l’API du compilateur](compiler-api-model.md)
- [Utiliser la syntaxe](work-with-syntax.md)
- [Utiliser la sémantique](work-with-semantics.md)
- [Utiliser un espace de travail](work-with-workspace.md)

Pour commencer, vous devez installer le kit **.NET Compiler Platform SDK** :

[!INCLUDE[interactive-note](~/includes/roslyn-installation.md)]

<!--

Turn this on as more of the conceptual content is in place:
- Try the [Quickstarts](quickstart/index.md) to create your first tutorial.
- Experiment with one of the [Tutorials](tutorials/index.md).
- Explore the [Samples](samples/index.md) to see some simple analyzers.
- Read the [Concepts](concepts/index.md) to understand the ideas behind analyzers and code fixes.

-->
