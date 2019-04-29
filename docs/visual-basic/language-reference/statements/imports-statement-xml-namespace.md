---
title: Imports, instruction - Namespace XML (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.ImportsXmlns
helpviewer_keywords:
- XML namespace [Visual Basic], importing
- imports [Visual Basic]
- Imports statement [Visual Basic]
- namespaces [Visual Basic], importing
ms.assetid: 1f4d50a6-08c7-4c2e-8206-ccae35fcd1b4
ms.openlocfilehash: 97d08113a37477add9d770b0a680c303fe7e3040
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61638955"
---
# <a name="imports-statement-xml-namespace"></a>Imports, instruction (espace de noms XML)
Importe des préfixes d’espace de noms XML pour une utilisation dans les littéraux XML et les propriétés d’axe XML.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
Imports <xmlns:xmlNamespacePrefix = "xmlNamespaceName">  
```  
  
## <a name="parts"></a>Composants  
 `xmlNamespacePrefix`  
 Optionnel. La chaîne par laquelle le langage XML éléments et attributs peuvent faire référence à `xmlNamespaceName`. Si aucun `xmlNamespacePrefix` est fourni, l’espace de noms XML importé est l’espace de noms XML par défaut. Doit être un identificateur XML valide. Pour plus d’informations, consultez [les attributs et les noms d’éléments XML déclarés](../../../visual-basic/programming-guide/language-features/xml/names-of-declared-xml-elements-and-attributes.md).  
  
 `xmlNamespaceName`  
 Obligatoire. La chaîne qui identifie l’espace de noms XML importé.  
  
## <a name="remarks"></a>Notes  
 Vous pouvez utiliser la `Imports` instruction pour définir des espaces de noms XML global que vous pouvez utiliser avec les littéraux XML et les propriétés d’axe XML, ou en tant que paramètres transmis à la `GetXmlNamespace` opérateur. (Pour plus d’informations sur l’utilisation de la `Imports` pour importer un alias qui peut être utilisé lorsque des noms de type sont utilisés dans votre code, consultez [instruction Imports (.NET Namespace et Type)](../../../visual-basic/language-reference/statements/imports-statement-net-namespace-and-type.md).) La syntaxe de déclaration d’espace de noms XML à l’aide de la `Imports` instruction est identique à la syntaxe utilisée dans XML. Par conséquent, vous pouvez copier une déclaration d’espace de noms à partir d’un fichier XML et l’utiliser dans un `Imports` instruction.  
  
 Préfixes d’espace de noms XML sont utiles lorsque vous souhaitez créer des éléments XML qui sont du même espace de noms à plusieurs reprises. Le préfixe d’espace de noms XML déclaré avec le `Imports` instruction est globale en ce sens qu’il est disponible à tout le code dans le fichier. Vous pouvez l’utiliser lorsque vous créez des littéraux d’éléments XML et lorsque vous accédez à des propriétés d’axe XML. Pour plus d’informations, consultez [XML élément littéral](../../../visual-basic/language-reference/xml-literals/xml-element-literal.md) et [propriétés d’axe XML](../../../visual-basic/language-reference/xml-axis/index.md).  
  
 Si vous définissez un espace de noms XML global sans préfixe d’espace de noms (par exemple, `Imports <xmlns="http://SomeNameSpace>"`), cet espace de noms est considéré comme l’espace de noms XML par défaut. L’espace de noms XML par défaut est utilisé pour les littéraux d’élément XML ou les propriétés d’axe d’attribut XML qui ne spécifient pas explicitement un espace de noms. L’espace de noms par défaut est également utilisé si l’espace de noms spécifié est l’espace de noms vide (autrement dit, `xmlns=""`). L’espace de noms XML par défaut ne s’applique pas aux attributs XML dans les littéraux XML ou à des propriétés d’axe d’attribut XML qui n’ont pas un espace de noms.  
  
 Espaces de noms XML qui sont définis dans un littéral XML, appelés *des espaces de noms XML local*, sont prioritaires sur les espaces de noms XML sont définis par le `Imports` instruction comme global. Les espaces de noms XML qui sont définies par le `Imports` instruction sont prioritaires sur les espaces de noms XML importé pour un projet Visual Basic. Si un littéral XML définit un espace de noms XML, cet espace de noms local ne s’applique pas aux expressions incorporées.  
  
 Espaces de noms XML globaux suivent les mêmes règles de portée et de définition en tant que les espaces de noms .NET Framework. Par conséquent, vous pouvez inclure un `Imports` instruction pour définir un espace de noms XML global partout où vous pouvez importer un espace de noms .NET Framework. Cela inclut les fichiers de code et les espaces de noms importés au niveau du projet. Pour plus d’informations sur les espaces de noms importés au niveau du projet, consultez [Page références, Concepteur de projets (Visual Basic)](/visualstudio/ide/reference/references-page-project-designer-visual-basic).  
  
 Chaque fichier source peut contenir un nombre quelconque de `Imports` instructions. Ces derniers doivent respecter les déclarations d’option, tel que le `Option Strict` instruction et doivent précéder les déclarations d’élément de programmation, tel que `Module` ou `Class` instructions.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant importe un espace de noms XML par défaut et un espace de noms XML identifié par le préfixe `ns`. Il crée ensuite des littéraux XML qui utilisent les deux espaces de noms.  
  
 [!code-vb[VbXMLSamples#45](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/Module1.vb#45)]  
  
 Ce code affiche le texte suivant :  
  
```xml  
<ns:outer xmlns="http://DefaultNamespace"   
          xmlns:ns="http://NewNamespace">  
  <ns:innerElement></ns:innerElement>  
  <siblingElement></siblingElement>  
  <innerElement />  
</ns:outer>  
```  
  
## <a name="example"></a>Exemple  
 L’exemple suivant importe le préfixe d’espace de noms XML `ns`. Il crée ensuite un littéral XML qui utilise le préfixe d’espace de noms et affiche le formulaire final de l’élément.  
  
 [!code-vb[VbXMLSamples#22](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/XMLSamples10.vb#22)]  
  
 Ce code affiche le texte suivant :  
  
```xml  
<ns:outer xmlns:ns="http://SomeNamespace">  
  <ns:middle xmlns:ns="http://NewNamespace">  
    <ns:inner1 />  
    <inner2 xmlns="http://SomeNamespace" />  
  </ns:middle>  
</ns:outer>  
```  
  
 Notez que le compilateur a converti le préfixe d’espace de noms XML à partir d’un préfixe global à une définition de préfixe local.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant importe le préfixe d’espace de noms XML `ns`. Il utilise ensuite le préfixe de l'espace de noms pour créer un littéral XML et accéder au premier nœud enfant avec le nom qualifié `ns:name`.  
  
 [!code-vb[VbXMLSamples#19](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbXMLSamples/VB/XMLSamples8.vb#19)]  
  
 Ce code affiche le texte suivant :  
  
 `Patrick Hines`  
  
## <a name="see-also"></a>Voir aussi

- [Littéral d’élément XML](../../../visual-basic/language-reference/xml-literals/xml-element-literal.md)
- [Propriétés d’axe XML](../../../visual-basic/language-reference/xml-axis/index.md)
- [Nom des attributs et des éléments XML déclarés](../../../visual-basic/programming-guide/language-features/xml/names-of-declared-xml-elements-and-attributes.md)
- [GetXmlNamespace (opérateur)](../../../visual-basic/language-reference/operators/getxmlnamespace-operator.md)
