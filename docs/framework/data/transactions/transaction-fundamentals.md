---
title: Notions de base des transactions
ms.date: 03/30/2017
ms.assetid: 353f4ee2-e6bf-4b1c-b1c8-385fc8a486c0
ms.openlocfilehash: 49e44ce1112a44c105f47560017331afe4454a0d
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61793514"
---
# <a name="transaction-fundamentals"></a>Notions de base des transactions
Les transactions servent à lier plusieurs tâches ensemble. Par exemple, imaginez qu'une application effectue deux tâches. Une table est d'abord créée dans une base de données. Un objet spécialisé est ensuite appelé pour collecter, formater et insérer des données dans la nouvelle table. Ces deux tâches sont liées et sont même interdépendantes. Cela vous évite de créer une nouvelle table sauf si vous devez y insérer des données. L'exécution des deux tâches au sein de l'étendue d'une seule transaction effectue la connexion entre les deux. Si la seconde tâche échoue, la première est restaurée à un point intervenant avant la création de la nouvelle table.  
  
 Pour garantir un comportement prévisible, toutes les transactions doivent posséder les propriétés ACID de base (atomicité, cohérence, isolation et durabilité). Ces propriétés renforcent le rôle des transactions fondamentales en tant que propositions tout-ou-rien. Pour plus d’informations sur ACID, consultez [propriétés ACID](https://go.microsoft.com/fwlink/?LinkId=98791). En résumé, les propriétés ACID garantissent la réussite ou l'échec d'un ensemble de tâches en tant qu'unité. En terminologie de traitement de transaction, une transaction est validée ou abandonnée. Pour qu'une transaction soit validée, tous les participants doivent s'assurer que chaque modification apportée aux données est permanente. Ces modifications doivent persister même en cas de panne du système ou de tout autre événement imprévu. Si l'un des participants seulement ne respecte pas cette garantie, l'intégralité de la transaction échoue. Toutes les modifications apportées aux données au sein de l'étendue de la transaction sont restaurées à un point spécifique.  
  
 Une transaction peut être restreinte à une seule ressource de données, telle qu'une base de données ou une file d'attente de messages. Dans ce cas, la transaction locale est gérée par le gestionnaire de transactions fourni par <xref:System.Transactions>, qui permet de générer un gain de performance. Contrôlées par la ressource de données, ces transactions sont efficaces et faciles à gérer.  
  
 Les transactions peuvent également couvrir plusieurs ressources de données. Les transactions distribuées permettent d'intégrer plusieurs opérations se produisant sur différents systèmes en une seule action de réussite ou d'échec. Dans ce cas, les transactions sont coordonnées par le MSDTC (Microsoft Distributed Transaction Coordinator) de chaque système.  
  
 Lors du développement d'une application transactionnelle à l'aide des classes fournies par <xref:System.Transactions>, il n'est pas nécessaire de s'interroger sur le type de transaction requise ou sur le gestionnaire de transactions concerné. L'infrastructure <xref:System.Transactions> gère automatiquement ces questions pour vous.  
  
 Lorsque vous créez une transaction, vous pouvez spécifier le niveau d'isolation qui s'y applique. Le niveau d’isolation, défini par le <xref:System.Transactions.IsolationLevel> enum, déterminent le niveau d’accès d’autres transactions seront ont aux données affectés par votre transaction.  
  
 Vous pouvez créer des transactions à l’aide d’ADO.NET, <xref:System.EnterpriseServices>, ou le modèle de programmation transactionnels fourni par le <xref:System.Transactions> espace de noms. Le [fonctionnalités fournies par System.Transactions](../../../../docs/framework/data/transactions/features-provided-by-system-transactions.md) rubrique traite des fonctionnalités que vous pouvez utiliser pour écrire une application transactionnelle à l’aide du <xref:System.Transactions> espace de noms.  
  
## <a name="see-also"></a>Voir aussi

- [Fonctionnalités fournies par System.Transactions](../../../../docs/framework/data/transactions/features-provided-by-system-transactions.md)
