---
title: การกรองข้อมูลขั้นสูงในที่เก็บ RCS/ส่วนกลาง
description: หัวข้อนี้จะอธิบายความสามารถในการกรองข้อมูลขั้นสูงสำหรับที่เก็บส่วนกลางของ RCS ซึ่งได้รับการปรับปรุงเพื่อรวมตัวกรองข้อมูลเพิ่มเติม
author: JaneA07
manager: AnnBe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 1adbd690795139778dc77a574e9d5f91a4bdeb3c
ms.sourcegitcommit: ff6dde637d2f5d2bd18a582eb41573d4c69acdd6
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/08/2020
ms.locfileid: "3249176"
---
# <a name="enhanced-filtering-options-for-finding-configurations-in-the-global-repository"></a><span data-ttu-id="3805d-103">ตัวเลือกการกรองข้อมูลขั้นสูงสำหรับการค้นหาการตั้งค่าคอนฟิกในที่เก็บส่วนกลาง</span><span class="sxs-lookup"><span data-stu-id="3805d-103">Enhanced filtering options for finding configurations in the Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3805d-104">หัวข้อนี้จะอธิบายความสามารถในการกรองข้อมูลขั้นสูงสำหรับที่เก็บส่วนกลางของ Regulatory Configuration Services (RCS) ซึ่งได้รับการปรับปรุงเพื่อรวมตัวกรองข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3805d-104">This topic describes enhanced filtering capabilities for Regulatory Configuration Services (RCS) Global repository, which have been improved to include the following filters:</span></span> 
- <span data-ttu-id="3805d-105">**ประเทศ/ภูมิภาค** - ตามรหัสประเทศ ISO</span><span class="sxs-lookup"><span data-stu-id="3805d-105">**Country/region** - based on ISO country codes</span></span>  
- <span data-ttu-id="3805d-106">**ป้าย** - สำหรับพื้นที่ทำงาน/คุณลักษณะ อุตสาหกรรม ชนิดเอกสารธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="3805d-106">**Tags** - for functional/feature area; Industry; Business document type</span></span> 

<span data-ttu-id="3805d-107">คุณสามารถใช้ตัวกรองโดยแยกต่างหากหรือในกลุ่ม อย่างใดอย่างหนึ่ง เพื่อค้นหาการตั้งค่าคอนฟิกที่ระบุหรือที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="3805d-107">You can apply filters, either individually or in groups, to find specific or related configurations.</span></span> <span data-ttu-id="3805d-108">ตัวอย่างเช่น ถ้าต้องการค้นหาเอกสารทางธุรกิจที่ตั้งค่าคอนฟิกได้ทั้งหมดที่เกี่ยวข้องกับใบแจ้งหนี้ของผู้จัดจำหน่าย คุณสามารถใช้ตัวกรองข้อมูล **ชนิดเอกสารทางธุรกิจ** ได้</span><span class="sxs-lookup"><span data-stu-id="3805d-108">For example, to find all configurable business documents related to vendor invoices, you can apply the **Business document type** filter.</span></span> 

<span data-ttu-id="3805d-109">คุณสามารถจำกัดการค้นหาเพิ่มเติมได้โดยการเลือกรหัสประเทศและการคลิก **ใช้ตัวกรองข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="3805d-109">You can further refine a search by selecting the country code and clicking **Apply filter**.</span></span>  

<span data-ttu-id="3805d-110">[![ส่วนตัวกรองสำหรับที่เก็บส่วนกลาง](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG)</span><span class="sxs-lookup"><span data-stu-id="3805d-110">[![Filter section for Global repository](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG)</span></span> 

<span data-ttu-id="3805d-111">ตัวอย่างต่อไปนี้แสดงผลลัพธ์เมื่อกรองข้อมูลใน **ชนิดเอกสารทางธุรกิจ**</span><span class="sxs-lookup"><span data-stu-id="3805d-111">The following example shows the results when filtering on **Business document type**.</span></span> 

<span data-ttu-id="3805d-112">[![ใช้ตัวกรองและนำเข้าสำหรับชนิดเอกสารทางธุรกิจ](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG)</span><span class="sxs-lookup"><span data-stu-id="3805d-112">[![Applied filter and Import for business document type](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG)</span></span> 

<span data-ttu-id="3805d-113">คุณสามารถนำเข้าผลลัพธ์ที่ถูกกรองไปยังผู้ใช้ RCS หรือสภาพแวดล้อม Dynamics 365 Finance อย่างใดอย่างหนึ่ง หรือเป็นชุด (โดยการเลือกกลุ่มการตั้งค่าคอนฟิก) และการคลิก **นำเข้า**</span><span class="sxs-lookup"><span data-stu-id="3805d-113">Filtered results can be imported into users RCS or Dynamics 365 Finance environment, either individually or as a set (by selecting the group of configurations) and clicking **Import**.</span></span>






