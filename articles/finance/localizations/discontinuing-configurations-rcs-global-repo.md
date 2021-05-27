---
title: ยกเลิกการกำหนดค่าคอนฟิกในที่เก็บส่วนกลางของ RCS
description: หัวข้อนี้จะอธิบายวิธีการยกเลิกการกำหนดค่าคอนฟิกในที่เก็บส่วนกลางของ RCS
author: JaneA07
ms.date: 02/17/2021
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
ms.search.validFrom: 2021-02-02
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 2bd22e991de376cfd93f75158f1f29716d2559e1
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018744"
---
# <a name="discontinue-configurations-in-the-rcs-global-repository"></a><span data-ttu-id="c47f6-103">ยกเลิกการกำหนดค่าคอนฟิกในที่เก็บส่วนกลางของ RCS</span><span class="sxs-lookup"><span data-stu-id="c47f6-103">Discontinue configurations in the RCS Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c47f6-104">หัวข้อนี้จะอธิบายวิธีการยกเลิกการกำหนดค่าคอนฟิกในที่เก็บส่วนกลางของ RCS</span><span class="sxs-lookup"><span data-stu-id="c47f6-104">This topic describes how to discontinue configuration in the RCS Global repository.</span></span> <span data-ttu-id="c47f6-105">ก่อนหน้านี้ สามารถลบได้เฉพาะการกำหนดค่าคอนฟิกที่ไม่ต้องการอีกต่อไปเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="c47f6-105">Previously, it was possible only to delete configurations that were no longer required.</span></span> <span data-ttu-id="c47f6-106">อย่างไรก็ตาม ขณะนี้คุณสามารถเลือกการกำหนดค่าคอนฟิกเป็น **ยกเลิก** ในที่เก็บส่วนกลางของ RCS</span><span class="sxs-lookup"><span data-stu-id="c47f6-106">However now you can mark a released configuration as **Discontinued** in the RCS Global repository.</span></span> <span data-ttu-id="c47f6-107">ด้วยฟังก์ชันนี้ คุณยังสามารถทำสิ่งต่อไปนี้ได้</span><span class="sxs-lookup"><span data-stu-id="c47f6-107">With this functionality, you can also do the following:</span></span> 
 
 - <span data-ttu-id="c47f6-108">ระบุการแจ้งเตือนล่วงหน้าเมื่อมีการวางแผนยกเลิกการกำหนดค่า</span><span class="sxs-lookup"><span data-stu-id="c47f6-108">Provide up front notifications when a configuration is planned to be discontinued.</span></span>
 - <span data-ttu-id="c47f6-109">รวมรายละเอียดที่เกี่ยวข้องกับการกำหนดค่าคอนฟิกแทนที่</span><span class="sxs-lookup"><span data-stu-id="c47f6-109">Include applicable details about the replacement configuration.</span></span>
 - <span data-ttu-id="c47f6-110">ตั้งค่า **รองรับจนถึง** วันที่สำหรับการกำหนดค่าคอนฟิกเฉพาะเพื่อแจ้งให้ผู้ใช้ทราบว่าจะเลิกใช้งานเมื่อใด</span><span class="sxs-lookup"><span data-stu-id="c47f6-110">Set a **Supported until** date for the specific configuration to inform the user when it will be discontinued.</span></span>

<span data-ttu-id="c47f6-111">เมื่อคุณยกเลิกเวอร์ชันการกำหนดค่าคอนฟิก คุณสามารถระบุข้อมูลเพิ่มเติมดังต่อไปนี้ได้</span><span class="sxs-lookup"><span data-stu-id="c47f6-111">When you discontinue a configuration version, you can specify the following optional information:</span></span>

  - <span data-ttu-id="c47f6-112">**การกำหนดค่าการเปลี่ยน**</span><span class="sxs-lookup"><span data-stu-id="c47f6-112">**Replacement configuration**</span></span>
  - <span data-ttu-id="c47f6-113">**เวอร์ชันการกำหนดค่าคอนฟิกแทนที่**</span><span class="sxs-lookup"><span data-stu-id="c47f6-113">**Replacement configuration version**</span></span>
  - <span data-ttu-id="c47f6-114">**หมายเหตุข้อความอิสระ** ใช้เขตข้อมูลนี้เพื่อให้มีลิงค์เอกสารหรือข้อมูลอ้างอิง</span><span class="sxs-lookup"><span data-stu-id="c47f6-114">**Free text note**: Use this field to provide documentation links or references</span></span>
  - <span data-ttu-id="c47f6-115">**รองรับจนถึง** เขตข้อมูลนี้แสดงวันที่ที่เสนอซึ่งรองรับการกำหนดค่าคอนฟิก/เวอร์ชันปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="c47f6-115">**Supported until**: This field provides the proposed date up to which the current configuration/version will be supported.</span></span> <span data-ttu-id="c47f6-116">ต้องอัพเดตวันที่นี้ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="c47f6-116">This date must be updated manually.</span></span>
  
<span data-ttu-id="c47f6-117">ในการยกเลิกการตั้งค่าคอนฟิก ให้ดําเนินการขั้นตอนต่อไปนี้ให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="c47f6-117">To discontinue the configuration, complete the following steps.</span></span> 

1. <span data-ttu-id="c47f6-118">เลือกว่าคุณต้องการยกเลิกการใช้เวอร์ชันเดียวหรือทุกเวอร์ชันด้วยการตั้งค่าเดียวกันภายใต้การดําเนินงานเดียวโดยตั้งค่า **เวอร์ชันทั้งหมด** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="c47f6-118">Select whether you want to discontinue a single version or all versions with the same settings in one operation by setting **All versions** to **Yes**.</span></span> 
2. <span data-ttu-id="c47f6-119">ตั้งค่าพารามิเตอร์ **ยกเลิก** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="c47f6-119">Set the **Discontinue** parameter to **Yes**.</span></span>
3. <span data-ttu-id="c47f6-120">เลือก **ตกลง** เพื่อยกเลิกการกำหนดค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="c47f6-120">Select **OK** to discontinue the configurations.</span></span> <span data-ttu-id="c47f6-121">เขตข้อมูล **วันที่ยกเลิก** จะถูกเติมเมื่อคุณบันทึกการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="c47f6-121">The **Discontinued date** field will be populated when you save the changes.</span></span>

![ยกเลิกข้อมูลการกำหนดค่าคอนฟิก](media/Discontinue-details-2.png)
  
<span data-ttu-id="c47f6-123">คุณสามารถแปลงการกำหนดค่าคอนฟิกกลับไปเป็น **ใช้ร่วมกัน** หรือปรับปรุงข้อมูลการยกเลิกได้ตลอดเวลา</span><span class="sxs-lookup"><span data-stu-id="c47f6-123">You can revert configuration back to **Shared** or adjust discontinuation information at any time.</span></span> <span data-ttu-id="c47f6-124">ถ้าคุณใช้การกำหนดค่าคอนฟิกร่วมกัน ให้ระบุ **รองรับจนถึง** วันที่และข้อมูลอื่นๆ ทั้งหมดที่เกี่ยวข้องกับการยกเลิกเพื่อระบุแผนของคุณสำหรับการยกเลิกในอนาคต</span><span class="sxs-lookup"><span data-stu-id="c47f6-124">If you share a configuration, specify the **Supported until** date and all other information related to the discontinuation to indicate your plans for future discontinuation.</span></span>

<span data-ttu-id="c47f6-125">หากคุณต้องการใช้ข้อมูลร่วมกันเกี่ยวกับแผนการยกเลิก ก่อนการยกเลิกการกำหนดค่าคอนฟิกจริง ผู้ใช้สามารถป้อนข้อมูลในเขตข้อมูลทั้งหมดที่เกี่ยวข้องกับการแทนที่ล่วงหน้าได้ แต่ปล่อยให้พารามิเตอร์ **การยกเลิก** ตั้งค่าเป็น **ไม่**</span><span class="sxs-lookup"><span data-stu-id="c47f6-125">If you want to share information about a planned discontinuation, prior to actually discontinuing the configuration, user is able to prefill all fields related to replacement but leave the **Discontinue** parameter set to **No**.</span></span>

> [!NOTE]
> <span data-ttu-id="c47f6-126">การยกเลิกไม่ได้จํากัดการดําเนินงานด้วยการกำหนดค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="c47f6-126">Discontinuation doesn't limit operations with configurations.</span></span> <span data-ttu-id="c47f6-127">คุณสามารถดำเนินการนําเข้า เรียกใช้ หรือสร้างการกำหนดค่าคอนฟิกต่อได้ เขตข้อมูลเหล่านี้เป็นข้อมูล</span><span class="sxs-lookup"><span data-stu-id="c47f6-127">You can continue to import, run, or derive the configurations, these fields are informational.</span></span>

## <a name="finance-supports-displaying-this-information-starting-in-version-10014"></a><span data-ttu-id="c47f6-128">การเงินรองรับการแสดงข้อมูลนี้โดยเริ่มตั้งแตเวอร์ชัน 10.0.14</span><span class="sxs-lookup"><span data-stu-id="c47f6-128">Finance supports displaying this information starting in version 10.0.14</span></span>

<span data-ttu-id="c47f6-129">การเริ่มต้นในเวอร์ชัน 10.0.14 Dynamics 365 Finance รองรับการแสดงข้อมูลการยกเลิกการทำงาน</span><span class="sxs-lookup"><span data-stu-id="c47f6-129">Starting in version 10.0.14, Dynamics 365 Finance supports displaying discontinuation information.</span></span> <span data-ttu-id="c47f6-130">บหน้า **ที่เก็บส่วนกลาง** คุณสามารถดูข้อมูลล่าสุดที่เกี่ยวข้องกับการยกเลิกได้</span><span class="sxs-lookup"><span data-stu-id="c47f6-130">On the **Global repository** page, you can view up to date information related to discontinuation.</span></span> <span data-ttu-id="c47f6-131">ตามค่าเริ่มต้น การกำหนดค่าคอนฟิกที่ถูกยกเลิกจะถูกกรองออก</span><span class="sxs-lookup"><span data-stu-id="c47f6-131">By default, configurations that are discontinued are filtered out.</span></span>
  
<span data-ttu-id="c47f6-132">หน้า **การกำหนดค่าคอนฟิกที่นำเข้า** (ERSolutionTable) จะแสดงการกำหนดค่าคอนฟิกที่ถูกยกเลิกไปแล้วเมื่อมีการนําเข้า</span><span class="sxs-lookup"><span data-stu-id="c47f6-132">The **Imported configurations** (ERSolutionTable) page, shows configurations that were already discontinued when there were imported.</span></span> <span data-ttu-id="c47f6-133">สำหรับการกำหนดค่าเหล่านั้นที่ถูกยกเลิกหลักการนำเข้า ข้อมูลการยกเลิกสามารถซิงโครไนซ์ได้โดยการดำเนินการงาน **อัพเดตการกำหนดค่าคอนฟิกการนําเข้า**</span><span class="sxs-lookup"><span data-stu-id="c47f6-133">For those configurations that were discontinued after import, the discontinuation information can be synchronized by running the **Import configurations updates** job.</span></span>


