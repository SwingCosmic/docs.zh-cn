---
title: "常用的集合类型"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-standard
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- collections [.NET Framework], generic
- objects [.NET Framework], grouping in collections
- generics [.NET Framework], collections
- IList interface, grouping data in collections
- IDictionary interface, grouping data in collections
- grouping data in collections, generic collection types
- Collections classes
- generic collections
ms.assetid: f5d4c6a4-0d7b-4944-a9fb-3b12d9ebfd55
caps.latest.revision: 29
author: mairaw
ms.author: mairaw
manager: wpickett
ms.translationtype: HT
ms.sourcegitcommit: b37d1d7ff75aebfcdf3e849931a5d2b3924d5d7a
ms.openlocfilehash: dfdfea20aeb8d0002ef22b9649afc09f80caeae2
ms.contentlocale: zh-cn
ms.lasthandoff: 09/06/2017

---
# <a name="commonly-used-collection-types"></a>常用的集合类型
集合类型是数据集合（如哈希表、队列、堆栈、包、字典和列表）的常见变体。  
  
 集合基于 <xref:System.Collections.ICollection> 接口、 <xref:System.Collections.IList> 接口、<xref:System.Collections.IDictionary> 接口或它们对应的泛型集合。 <xref:System.Collections.IList> 接口和 <xref:System.Collections.IDictionary> 接口都派生自 <xref:System.Collections.ICollection> 接口：因此，所有集合都直接或间接基于 <xref:System.Collections.ICollection> 接口。 在基于 <xref:System.Collections.IList> 接口（比如 <xref:System.Array>、<xref:System.Collections.ArrayList> 或 <xref:System.Collections.Generic.List%601>）或直接基于 <xref:System.Collections.ICollection> 接口（比如 <xref:System.Collections.Queue>、<xref:System.Collections.Concurrent.ConcurrentQueue%601>、<xref:System.Collections.Stack>、<xref:System.Collections.Concurrent.ConcurrentStack%601> 或 <xref:System.Collections.Generic.LinkedList%601>）的集合里，每个元素都只有一个值。 在基于 <xref:System.Collections.IDictionary> 接口（比如 <xref:System.Collections.Hashtable> 和 <xref:System.Collections.SortedList> 类，<xref:System.Collections.Generic.Dictionary%602> 和<xref:System.Collections.Generic.SortedList%602> 泛型类）或 <xref:System.Collections.Concurrent.ConcurrentDictionary%602> 类的集合中，每个元素都有一个键和一个值。  <xref:System.Collections.ObjectModel.KeyedCollection%602> 类是唯一的，因为它是值中嵌键的值的列表，因此，它的行为类似列表和字典。  
  
 泛型集合都是强类型的最佳解决方案。 但，如果你的语言不支持泛型，那么 <xref:System.Collections> 命名空间包含基集合，如 <xref:System.Collections.CollectionBase>、<xref:System.Collections.ReadOnlyCollectionBase> 和 <xref:System.Collections.DictionaryBase>，这些集合都是可扩展以创建强类型集合类的抽象基类。 需要高效的多线程集合访问时，请使用 <xref:System.Collections.Concurrent> 命名空间中的泛型集合。  
  
 集合会因元素的存储方式、排序方式、执行搜索的方式以及比较方式的不同而不同。 <xref:System.Collections.Queue> 类和 <xref:System.Collections.Generic.Queue%601> 泛型类提供先进先出列表，而 <xref:System.Collections.Stack> 类和 <xref:System.Collections.Generic.Stack%601> 泛型类提供后进先出列表。 <xref:System.Collections.SortedList> 类和 <xref:System.Collections.Generic.SortedList%602> 泛型类提供 <xref:System.Collections.Hashtable> 类和 <xref:System.Collections.Generic.Dictionary%602> 泛型类的已排序版本。 <xref:System.Collections.Hashtable> 或 <xref:System.Collections.Generic.Dictionary%602> 的元素只能通过元素的键访问，但 <xref:System.Collections.SortedList> 或 <xref:System.Collections.ObjectModel.KeyedCollection%602> 的元素能通过元素的键或索引访问。 所有集合中的索引都从零开始，<xref:System.Array> 除外，它允许不从零开始的数组。  
  
 LINQ to Objects 功能让你可以通过使用 LINQ 查询来访问内存中的对象，条件是该对象类型实现 <xref:System.Collections.IEnumerable> 或 <xref:System.Collections.Generic.IEnumerable%601>。 LINQ 查询提供了一种通用的数据访问模式；与标准 `foreach` 循环相比，它通常更加简洁，可读性更高；这种查询可提供筛选、排序和分组功能。 LINQ 查询还可提高性能。 有关详细信息，请参阅 [LINQ to Objects](http://msdn.microsoft.com/library/73cafe73-37cf-46e7-bfa7-97c7eea7ced9) 和[并行 LINQ (PLINQ)](../../../docs/standard/parallel-programming/parallel-linq-plinq.md)。  
  
## <a name="related-topics"></a>相关主题  
  
|标题|说明|  
|-----------|-----------------|  
|[集合和数据结构](../../../docs/standard/collections/index.md)|讨论 [!INCLUDE[dnprdnshort](../../../includes/dnprdnshort-md.md)] 中的各种集合类型，包括堆栈、队列、列表、数组和字典。|  
|[哈希表和字典集合类型](../../../docs/standard/collections/hashtable-and-dictionary-collection-types.md)|描述泛型和非泛型的基于哈希的字典类型的功能。|  
|[已排序的集合类型](../../../docs/standard/collections/sorted-collection-types.md)|描述为列表和集提供排序功能的类。|  
|[泛型](../../../docs/standard/generics/index.md)|描述泛型功能，包括 [!INCLUDE[dnprdnshort](../../../includes/dnprdnshort-md.md)] 提供的泛型集合、委托和接口。 为 C#、Visual Basic 和 Visual C++ 提供功能文档链接和支持技术（如反射）链接。|  
  
## <a name="reference"></a>参考  
 <xref:System.Collections?displayProperty=fullName>  
  
 <xref:System.Collections.Generic?displayProperty=fullName>  
  
 <xref:System.Collections.ICollection?displayProperty=fullName>  
  
 <xref:System.Collections.Generic.ICollection%601?displayProperty=fullName>  
  
 <xref:System.Collections.IList?displayProperty=fullName>  
  
 <xref:System.Collections.Generic.IList%601?displayProperty=fullName>  
  
 <xref:System.Collections.IDictionary?displayProperty=fullName>  
  
 <xref:System.Collections.Generic.IDictionary%602?displayProperty=fullName>

