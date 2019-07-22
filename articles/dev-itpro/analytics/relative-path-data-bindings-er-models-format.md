---
title: ใช้พาธสัมพัทธ์ในการผูกข้อมูลของแบบจำลองและรูปแบบ ER
description: .
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable , ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6582cca9b912868f88de2770a17cbb6e67328660
ms.sourcegitcommit: d0fa7eb2166a30314205e7f70bbeaff6fbd5fb55
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/03/2019
ms.locfileid: "1726563"
---
# <a name="use-a-relative-path-in-data-bindings-of-er-models-and-formats"></a><span data-ttu-id="909c7-103">ใช้พาธสัมพัทธ์ในการผูกข้อมูลของแบบจำลองและรูปแบบ ER</span><span class="sxs-lookup"><span data-stu-id="909c7-103">Use a relative path in data bindings of ER models and formats</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="909c7-104">เครื่องมือการรายงานทางอิเล็กทรอนิกส์ (ER) ช่วยให้ผู้ใช้สามารถกำหนดโครงสร้างรูปแบบอิเล็กทรอนิกส์ แล้วอธิบายวิธีที่ควรจะเติมโครงสร้างดังกล่าวโดยใช้ข้อมูลและอัลกอริทึมที่มีอยู่ใน Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="909c7-104">The Electronic reporting (ER) tool lets users define electronic format structures and then describe how those structures should be filled by using data and algorithms that exist in Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="909c7-105">สำหรับข้อมูลเพิ่มเติม โปรดดู [สร้างการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์ (ER)](electronic-reporting-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="909c7-105">For more information, see [Create Electronic reporting (ER) configurations](electronic-reporting-configuration.md).</span></span> <span data-ttu-id="909c7-106">เมื่อต้องการระบุโฟลว์ของข้อมูลสำหรับการดึงข้อมูล Finance and Operations และการใช้เพื่อสร้างเอกสารอิเล็กทรอนิกส์ คุณต้องทำสิ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="909c7-106">To specify the data flow for retrieving Finance and Operations data and using it to generate  an electronic document, you need to do the following:</span></span>

- <span data-ttu-id="909c7-107">ผูกแหล่งข้อมูลที่ตั้งค่าคอนฟิกกับองค์ประกอบของแบบจำลองข้อมูลเฉพาะโดเมนที่ออกแบบไว้</span><span class="sxs-lookup"><span data-stu-id="909c7-107">Bind configured data sources to elements of the designed domain-specific data model.</span></span> <span data-ttu-id="909c7-108">โครงสร้างแบบจำลองและแหล่งข้อมูลที่เลือกอาจเป็นส่วนหนึ่งของโครงสร้างตามลำดับชั้นที่ซับซ้อน</span><span class="sxs-lookup"><span data-stu-id="909c7-108">The model structure and selected data sources might be part of a complex hierarchical structure.</span></span> <span data-ttu-id="909c7-109">ด้วยเหตุผลนี้ การผูกครั้งสุดท้ายอาจมีขนาดค่อนข้างใหญ่และมีองค์ประกอบหลายชนิดที่แตกต่างกัน (ตัวอย่างเช่น ความสัมพันธ์ ตาราง และวิธีการ)</span><span class="sxs-lookup"><span data-stu-id="909c7-109">Because of this, final bindings can be quite large and contain many elements of different types (for example, relations, tables, and methods,).</span></span> <span data-ttu-id="909c7-110">การผูกจะสามารถอ่านได้น้อยลงและค่อนข้างซับซ้อนในการตรวจทานและทำความเข้าใจ โดยเฉพาะอย่างยิ่งสำหรับผู้ที่ไม่ใช่เจ้าของ</span><span class="sxs-lookup"><span data-stu-id="909c7-110">The bindings can become less readable and quite complex to review and understand, especially for non-owners.</span></span> 
- <span data-ttu-id="909c7-111">ผูกองค์ประกอบแบบจำลองข้อมูลกับส่วนประกอบของรูปแบบ เพื่อกำหนดข้อมูลที่จะมีการเติมข้อมูลจากแบบจำลองข้อมูลไปยังเอาท์พุทของรูปแบบที่สร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="909c7-111">Bind data model elements with format components to define what data will be populated from the data model to the generated format’s output.</span></span>

<span data-ttu-id="909c7-112">เมื่อต้องการปรับปรุงการใช้งานของโปรแกรมออกแบบการแม็ป ER คุณลักษณะของพาธสัมพัทธ์ได้ถูกนำออกใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="909c7-112">To improve usability of ER mapping designers, the relative path feature has been released.</span></span> <span data-ttu-id="909c7-113">โดยค่าเริ่มต้น ตัวเลือกการแสดงพาธสัมพัทธ์จะถูกเปิดใช้งานสำหรับอินสแตนซ์ใหม่ใดๆ ของ Finance and Operations ที่ซึ่งมีการเปิดใช้งานประสบการณ์การออกแบบ ER (Microsoft Dynamics 365 for Finance and operations Microsoft Regulatory Configuration Service)</span><span class="sxs-lookup"><span data-stu-id="909c7-113">By default, the relative path representation option is turned on for any new instance of Finance and Operations where ER design experience is enabled (Microsoft Dynamics 365 for Finance and operations, Microsoft Regulatory Configuration Service).</span></span> <span data-ttu-id="909c7-114">เราดำเนินการพารามิเตอร์พาธสัมพัทธ์ เพื่อให้ผู้ใช้สามารถใช้พาธแบบเต็มเมื่อทำงานกับการนำเสนอของการผูก ER นี้ได้</span><span class="sxs-lookup"><span data-stu-id="909c7-114">We implemented the relative path parameter so that users can keep using the full path when work with this presentation of ER bindings.</span></span>

<span data-ttu-id="909c7-115">[![พารามิเตอร์ผู้ใช้](./media/relative-path-01.png)](./media/relative-path-01.png)</span><span class="sxs-lookup"><span data-stu-id="909c7-115">[![User parameters](./media/relative-path-01.png)](./media/relative-path-01.png)</span></span>

 
<span data-ttu-id="909c7-116">เมื่อมีการเปิดใช้งานพารามิเตอร์การใช้พาธสัมพัทธ์ อักขระ @ เดียวจะแทนที่พาธเป็นรายการหลักในการผูกข้อมูลขององค์ประกอบแบบจำลองปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="909c7-116">When the relative path usage parameter is turned on, a single @ character replaces the path to the parent item in the binding of the current model element.</span></span> <span data-ttu-id="909c7-117">พาธการผูกข้อมูลทั้งหมดจะสั้นลง ซึ่งทำให้การแม็ปทั้งหมดชัดเจนและเข้าใจง่ายขึ้น</span><span class="sxs-lookup"><span data-stu-id="909c7-117">The entire binding path becomes shorter, which makes the entire mapping more obvious and easier to understand.</span></span> <span data-ttu-id="909c7-118">ในกรณีส่วนใหญ่ จะไม่ต้องการการเลื่อนเพิ่มเติมในตัวออกแบบ ER เพื่อดูการผูกทั้งหมดของแบบจำลองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="909c7-118">In most cases, no additional scrolling is required in the ER designer to view all the bindings of the data model.</span></span>

<span data-ttu-id="909c7-119">[![ตัวออกแบบการแม็ปแบบจำลอง](./media/relative-path-02.png)](./media/relative-path-02.png)</span><span class="sxs-lookup"><span data-stu-id="909c7-119">[![Model mapping designer](./media/relative-path-02.png)](./media/relative-path-02.png)</span></span>
 
<span data-ttu-id="909c7-120">เมื่อคุณเริ่มต้นการออกแบบนิพจน์ ER ใหม่ คุณต้องป้อนอักขระเดียวเท่านั้นเพื่อกำหนดการผูกกับฟิลด์ของรายการหลัก</span><span class="sxs-lookup"><span data-stu-id="909c7-120">When you start designing a new ER expression, you need to enter only one character to define a binding to a field of the parent item.</span></span>

<span data-ttu-id="909c7-121">[![โปรแกรมออกแบบสูตร](./media/relative-path-03.png)](./media/relative-path-03.png)</span><span class="sxs-lookup"><span data-stu-id="909c7-121">[![Formula designer](./media/relative-path-03.png)](./media/relative-path-03.png)</span></span>
 
<span data-ttu-id="909c7-122">เมื่อคุณตัดสินใจที่จะเปลี่ยนแหล่งข้อมูลของรายการแบบจำลองหลัก ที่มีการใช้เส้นทางสัมบูรณ์ คุณต้องผูกรายการแบบจำลองนี้ด้วยตนเองอีกครั้ง เช่นเดียวกับสินค้าที่ซ้อนกันทั้งหมด ไปยังแหล่งข้อมูลใหม่</span><span class="sxs-lookup"><span data-stu-id="909c7-122">When you decide to change the data source of the parent model item, with absolute path usage, you have to manually rebind this model item, as well as all nested items, to a new data source.</span></span> <span data-ttu-id="909c7-123">เมื่อเปิดการใช้งานพาธสัมพัทธ์ และคุณเลือกแหล่งข้อมูลใหม่ที่จะผูกกับรายการหลัก คุณจะมีตัวเลือกในการผูกองค์ประกอบที่ซ้อนทั้งหมดของรายการหลักนี้อีกครั้งโดยอัตโนมัติด้วยการคลิกครั้งเดียว</span><span class="sxs-lookup"><span data-stu-id="909c7-123">When relative path usage is turned on, and you select a new data source to be bound to a parent item, you are offered an option to automatically rebind all nested elements of this parent item with one click.</span></span>

<span data-ttu-id="909c7-124">[![แทนที่ข้อความพาธที่มีอยู่](./media/relative-path-04.png)](./media/relative-path-04.png)</span><span class="sxs-lookup"><span data-stu-id="909c7-124">[![Replace existing path message](./media/relative-path-04.png)](./media/relative-path-04.png)</span></span>
 
<span data-ttu-id="909c7-125">ถ้าคุณยืนยันการผูกของรายการที่ซ้อนกันอีกครั้ง รายการหลักใหม่จะถูกวางไปยังพาธของรายการที่ซ้อนกันแต่ละรายการซึ่งมีรายการหลักที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="909c7-125">If you confirm rebinding of nested items, the new parent item will be placed to the path of each nested item containing the existing parent item.</span></span>
<span data-ttu-id="909c7-126">คุณลักษณะนี้ไม่แบ่งความเข้ากันได้แบบย้อนหลังของโครงสร้าง ER</span><span class="sxs-lookup"><span data-stu-id="909c7-126">This feature does not break the backward compatibility of the ER framework.</span></span> <span data-ttu-id="909c7-127">การตั้งค่าคอนฟิก ER ที่ออกแบบมาก่อนหน้านี้ทั้งหมดจะทำงานกับคุณลักษณะใหม่นี้ และไม่จำเป็นต้องมีการปรับปรุงหรือการแปลง</span><span class="sxs-lookup"><span data-stu-id="909c7-127">All previously designed ER configurations will work with this new feature, and no upgrades or conversions are required.</span></span>

> [!NOTE]
> <span data-ttu-id="909c7-128">การเปลี่ยนแปลงทั้งหมดที่นำมาใช้โดยการปรับเปลี่ยนโดยรวมของการผูกขององค์ประกอบที่ซ้อนกันในการแม็ปแบบจำลอง จะถูกบันทึกอย่างถูกต้องในส่วนที่แตกต่างของการตั้งค่าคอนฟิก (การติดตามการเปลี่ยนแปลง)</span><span class="sxs-lookup"><span data-stu-id="909c7-128">All changes that are introduced by mass modification of bindings of nested elements in model mappings are correctly saved in a configuration delta (trace of changes).</span></span> <span data-ttu-id="909c7-129">นี่จะช่วยให้ลูกค้าสามารถปรับใช้ซ้ำรุ่นที่สืบทอดมาของการแม็ปแบบจำลองไปยังรุ่นฐานใหม่ใดๆ ที่มีการแก้ไขโดยใช้คุณลักษณะใหม่นี้</span><span class="sxs-lookup"><span data-stu-id="909c7-129">This allows customers to rebase their derived version of model mappings to any new base version of it that has been modified by using this new feature.</span></span>
