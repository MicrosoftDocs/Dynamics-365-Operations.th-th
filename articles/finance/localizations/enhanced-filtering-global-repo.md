---
title: การกรองข้อมูลขั้นสูงของ RCS ในที่เก็บ RCS/ส่วนกลาง
description: หัวข้อนี้จะอธิบายความสามารถในการกรองข้อมูลขั้นสูงสำหรับที่เก็บส่วนกลางของ RCS ซึ่งได้รับการปรับปรุงเพื่อรวมตัวกรองข้อมูลเพิ่มเติม
author: JaneA07
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 31df79159caa1094a68743ba07f308a2029e4071
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832655"
---
# <a name="rcs-enhanced-filtering-options-for-finding-configurations-in-the-rcsglobal-repository"></a><span data-ttu-id="b9199-103">ตัวเลือกการกรองข้อมูลขั้นสูงของ RCS สำหรับการค้นหาการตั้งค่าคอนฟิกในที่เก็บ RCS/ส่วนกลาง</span><span class="sxs-lookup"><span data-stu-id="b9199-103">RCS enhanced filtering options for finding configurations in the RCS/Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b9199-104">หัวข้อนี้จะอธิบายความสามารถในการกรองข้อมูลขั้นสูงสำหรับที่เก็บส่วนกลางของ Regulatory Configuration Services (RCS) ซึ่งได้รับการปรับปรุงเพื่อรวมความสามารถในการกรองเงื่อนไขต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b9199-104">This topic describes enhanced filtering capabilities for Regulatory Configuration Services (RCS) Global repository, which have been improved to include the ability to filter with the following criteria:</span></span> 
- <span data-ttu-id="b9199-105">**ประเทศ/ภูมิภาค** - ตามรหัสประเทศ ISO</span><span class="sxs-lookup"><span data-stu-id="b9199-105">**Country/region** - Based on ISO country codes</span></span>  
- <span data-ttu-id="b9199-106">ชนิด **แท็ก** สำหรับ:</span><span class="sxs-lookup"><span data-stu-id="b9199-106">**Tags** types for:</span></span>
  - <span data-ttu-id="b9199-107">พื้นที่ฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="b9199-107">Functional area</span></span>
  - <span data-ttu-id="b9199-108">พื้นที่คุณลักษณะ</span><span class="sxs-lookup"><span data-stu-id="b9199-108">Feature area</span></span>
  - <span data-ttu-id="b9199-109">อุตสาหกรรม</span><span class="sxs-lookup"><span data-stu-id="b9199-109">Industry</span></span> 
  - <span data-ttu-id="b9199-110">เอกสารทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="b9199-110">Business document</span></span> 

<span data-ttu-id="b9199-111">เพื่อทำให้ง่ายขึ้นในการค้นหาการตั้งค่าคอนฟิกที่ระบุหรือที่เกี่ยวข้อง คุณสามารถใช้ตัวกรองโดยแยกต่างหาก หรือเป็นกลุ่ม อย่างใดอย่างหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="b9199-111">To make it easier to discover specific or related configurations you can apply filters, either individually or as a group.</span></span> <span data-ttu-id="b9199-112">ตัวอย่างเช่น ถ้าต้องการค้นหาชนิดเดียวของเอกสารทางธุรกิจที่สามารถตั้งค่าคอนฟิกได้ซึ่งเกี่ยวข้องใบแจ้งหนี้ของผู้จัดจำหน่าย คุณสามารถใช้ตัวกรอง **ชนิดเอกสารทางธุรกิจ** เพื่อค้นหาชนิดของเอกสารนั้นได้</span><span class="sxs-lookup"><span data-stu-id="b9199-112">For example, to find a single type of 'configurable business documents that are related to vendor invoices, you could apply a **Business document type** filter to search for that type of document.</span></span> 

<span data-ttu-id="b9199-113">[![ส่วนตัวกรองสำหรับที่เก็บส่วนกลาง](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG)</span><span class="sxs-lookup"><span data-stu-id="b9199-113">[![Filter section for Global repository](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG)</span></span> 

<span data-ttu-id="b9199-114">คุณสามารถปรับปรุงการค้นหาได้ด้วยการเลือกชนิดเอกสาร ตัวอย่างเช่น 'ใบแจ้งหนี้ของผู้จัดจำหน่าย' และคลิก **ใช้ตัวกรองข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="b9199-114">You can further refine the search by selecting document type, for example 'vendor invoice' and clicking **Apply filter**.</span></span> <span data-ttu-id="b9199-115">ตัวอย่างต่อไปนี้แสดงผลลัพธ์เมื่อกรองข้อมูลใน **ชนิดเอกสารทางธุรกิจ** ด้วยชนิดเอกสารที่เพิ่ม</span><span class="sxs-lookup"><span data-stu-id="b9199-115">The following example shows the results when filtering on **Business document type** with the document type added.</span></span> 

<span data-ttu-id="b9199-116">[![ใช้ตัวกรองและนำเข้าสำหรับชนิดเอกสารทางธุรกิจ](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG)</span><span class="sxs-lookup"><span data-stu-id="b9199-116">[![Applied filter and Import for business document type](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG)</span></span> 

<span data-ttu-id="b9199-117">คุณสามารถนำเข้าผลลัพธ์ที่ถูกกรองเข้าไปในที่เก็บ RCS ของผู้ใช้หรือสภาพแวดล้อม Dynamics 365 Finance อย่างใดอย่างหนึ่ง ทีละรายการ หรือเป็นชุด</span><span class="sxs-lookup"><span data-stu-id="b9199-117">Filtered results can be imported into a users RCS repository or a Dynamics 365 Finance environment, either individually or as a set.</span></span> <span data-ttu-id="b9199-118">เมื่อต้องการดำเนินการนี้ ให้เลือกกลุ่มการตั้งค่าคอนฟิก และคลิก **นำเข้า**</span><span class="sxs-lookup"><span data-stu-id="b9199-118">To do this, select the group of configurations, and click **Import**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]