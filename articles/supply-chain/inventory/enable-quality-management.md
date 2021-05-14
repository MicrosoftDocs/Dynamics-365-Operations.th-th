---
title: เปิดใช้งานการจัดการคุณภาพและความไม่สอดคล้องกัน
description: หัวข้อนี้แสดงภาพรวมของกระบวนการสำหรับการตั้งค่าและการตั้งค่าคอนฟิกคุณลักษณะการจัดการคุณภาพและความไม่สอดคล้องกันใน Microsoft Dynamics 365 Supply Chain Management
author: perlynne
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome, InventParameters, InventProblemType, InventProblemTypeSetup, InventQuarantineZone, InventTestDiagnosticType, InventTestReportSetup, SysUserManagement, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 67d5da648e31d07d054246f5d308a6c6cdeb506c
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956265"
---
# <a name="enable-quality-and-nonconformance-management"></a><span data-ttu-id="6bc27-103">เปิดใช้งานการจัดการคุณภาพและความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="6bc27-103">Enable quality and nonconformance management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6bc27-104">หัวข้อนี้แสดงภาพรวมของกระบวนการสำหรับการตั้งค่าและการตั้งค่าคอนฟิกคุณลักษณะการจัดการคุณภาพและความไม่สอดคล้องกันใน Microsoft Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="6bc27-104">This topic provides an overview of the process for setting up and configuring quality and nonconformance management features in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="enable-quality-and-nonconformance-management"></a><a name="enable-qm"></a><span data-ttu-id="6bc27-105">เปิดใช้งานการจัดการคุณภาพและความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="6bc27-105">Enable quality and nonconformance management</span></span>

<span data-ttu-id="6bc27-106">ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อเปิดใช้งานการจัดการคุณภาพบนระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="6bc27-106">Follow these steps to enable quality management on your system.</span></span>

1. <span data-ttu-id="6bc27-107">ไปที่ **การจัดการสินค้าคงคลัง \> การตั้งค่า \> พารามิเตอร์สินค้าคงคลังและการจัดการคลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="6bc27-107">Go to **Inventory management \> Setup \> Inventory and warehouse management parameters**.</span></span>
1. <span data-ttu-id="6bc27-108">บนแท็บ **การจัดการคุณภาพ** ให้ตั้งค่าตัวเลือก **ใช้การจัดการคุณภาพ** เป็น *ใช่*</span><span class="sxs-lookup"><span data-stu-id="6bc27-108">On the **Quality management** tab, set the **Use quality management** option to *Yes*.</span></span>
1. <span data-ttu-id="6bc27-109">ในฟิลด์ **อัตราต่อชั่วโมง** ป้อนอัตราค่าแรงต่อชั่วโมงในสกุลเงินท้องถิ่น</span><span class="sxs-lookup"><span data-stu-id="6bc27-109">In the **Hourly rate** field, enter an hourly labor rate in the local currency.</span></span> <span data-ttu-id="6bc27-110">อัตราต่อชั่วโมงจะถูกใช้ในการคำนวณต้นทุนสำหรับการดำเนินงานที่เกี่ยวข้องกับความไม่สอดคล้อง</span><span class="sxs-lookup"><span data-stu-id="6bc27-110">The hourly rate is used to calculate costs for operations that are related to a nonconformance.</span></span> <span data-ttu-id="6bc27-111">อัตราต่อชั่วโมงและต้นทุนที่คำนวณได้ให้การอ้างอิงข้อมูลสำหรับความไม่สอดคล้อง</span><span class="sxs-lookup"><span data-stu-id="6bc27-111">The hourly rate and calculated costs provide reference information for a nonconformance.</span></span> <span data-ttu-id="6bc27-112">จะไม่สัมพันธ์กับฟังก์ชันอื่น</span><span class="sxs-lookup"><span data-stu-id="6bc27-112">They don't interact with other functionality.</span></span>
1. <span data-ttu-id="6bc27-113">เลือก **การตั้งค่ารายงาน**</span><span class="sxs-lookup"><span data-stu-id="6bc27-113">Select **Report setup**.</span></span>
1. <span data-ttu-id="6bc27-114">เพิ่มบรรทัดใหม่ให้กับรายงานชนิดต่างๆ และเลือกชนิดของเอกสารที่จะใช้สำหรับรายงานแต่ละฉบับ</span><span class="sxs-lookup"><span data-stu-id="6bc27-114">Add new lines for the various report types, and select the type of document to use for each report.</span></span>
1. <span data-ttu-id="6bc27-115">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6bc27-115">Close the page.</span></span>
1. <span data-ttu-id="6bc27-116">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="6bc27-116">Close the page.</span></span>

## <a name="quality-management-configuration-process"></a><span data-ttu-id="6bc27-117">กระบวนการตั้งค่าคอนฟิกการจัดการคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="6bc27-117">Quality management configuration process</span></span>

<span data-ttu-id="6bc27-118">ก่อนที่คุณสามารถเริ่มใช้คุณลักษณะการจัดการคุณภาพและสร้างใบสั่งตรวจสอบคุณภาพได้ คุณต้องตั้งค่าคอนฟิกระบบและข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="6bc27-118">Before you can start to use the quality management features and generate quality orders, you must configure the system and prerequisites.</span></span> <span data-ttu-id="6bc27-119">ต่อไปนี้เป็นรายการขั้นตอนที่ต้องใช้ในการตั้งค่าคอนฟิกการจัดการคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="6bc27-119">Here is a list of the steps that are required to configure quality management.</span></span>

1. <span data-ttu-id="6bc27-120">[เปิดใช้งานการจัดการคุณภาพและความไม่สอดคล้องกัน](#enable-qm)</span><span class="sxs-lookup"><span data-stu-id="6bc27-120">[Enable quality and nonconformance management](#enable-qm).</span></span>
1. <span data-ttu-id="6bc27-121">ไม่ระบุ: [ตั้งค่าคอนฟิกเครื่องมือทดสอบ](quality-test-instruments.md)</span><span class="sxs-lookup"><span data-stu-id="6bc27-121">Optional: [Configure test instruments](quality-test-instruments.md).</span></span>
1. <span data-ttu-id="6bc27-122">[ตั้งค่าคอนฟิกการทดสอบ](quality-tests.md)</span><span class="sxs-lookup"><span data-stu-id="6bc27-122">[Configure tests](quality-tests.md).</span></span>
1. <span data-ttu-id="6bc27-123">[ตั้งค่าคอนฟิกตัวแปรทดสอบและผลที่ได้](quality-test-variables.md)</span><span class="sxs-lookup"><span data-stu-id="6bc27-123">[Configure test variables and outcomes](quality-test-variables.md).</span></span>
1. <span data-ttu-id="6bc27-124">[ตั้งค่าคอนฟิกกลุ่มทดสอบ](quality-test-groups.md)</span><span class="sxs-lookup"><span data-stu-id="6bc27-124">[Configure test groups](quality-test-groups.md).</span></span>
1. <span data-ttu-id="6bc27-125">ไม่ระบุ: [ตั้งค่าคอนฟิกกลุ่มคุณภาพ และเชื่อมโยงกับผลิตภัณฑ์](quality-groups.md)</span><span class="sxs-lookup"><span data-stu-id="6bc27-125">Optional: [Configure quality groups, and link to products](quality-groups.md).</span></span>
1. <span data-ttu-id="6bc27-126">ไม่ระบุ: [ตั้งค่าคอนฟิกการเชื่อมโยงคุณภาพ](quality-associations.md)</span><span class="sxs-lookup"><span data-stu-id="6bc27-126">Optional: [Configure quality associations](quality-associations.md).</span></span>

<span data-ttu-id="6bc27-127">หลังจากเสร็จสิ้นการตั้งค่าคอนฟิกแล้ว คุณสามารถเริ่มต้นสร้างและประมวลผลใบสั่งตรวจสอบคุณภาพได้</span><span class="sxs-lookup"><span data-stu-id="6bc27-127">After the configuration is completed, you can start to create and process quality orders.</span></span> <span data-ttu-id="6bc27-128">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการสร้างงานที่มีใบสั่งตรวจสอบคุณภาพ โปรดดู [ใบสั่งตรวจสอบคุณภาพ](quality-orders.md)</span><span class="sxs-lookup"><span data-stu-id="6bc27-128">For more information about how to create and work with quality orders, see [Quality orders](quality-orders.md).</span></span>

## <a name="nonconformance-management-configuration-process"></a><span data-ttu-id="6bc27-129">กระบวนการตั้งค่าคอนฟิกการจัดการความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="6bc27-129">Nonconformance management configuration process</span></span>

<span data-ttu-id="6bc27-130">ก่อนที่คุณสามารถเริ่มใช้คุณลักษณะการจัดการความไม่สอดคล้องกันและสร้างความไม่สอดคล้องกันได้ คุณต้องตั้งค่าคอนฟิกระบบและข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="6bc27-130">Before you can start to use the nonconformance management features and generate nonconformances, you must configure the system and prerequisites.</span></span> <span data-ttu-id="6bc27-131">ต่อไปนี้เป็นรายการขั้นตอนที่ต้องใช้ในการตั้งค่าคอนฟิกการจัดการความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="6bc27-131">Here is a list of the steps that are required to configure nonconformance management.</span></span>

1. <span data-ttu-id="6bc27-132">[เปิดใช้งานการจัดการคุณภาพและความไม่สอดคล้องกัน](#enable-qm)</span><span class="sxs-lookup"><span data-stu-id="6bc27-132">[Enable quality and nonconformance management](#enable-qm).</span></span>
1. <span data-ttu-id="6bc27-133">[ตั้งค่าคอนฟิกผู้ปฏิบัติงานที่รับผิดชอบการอนุมัติความไม่สอดคล้องกัน](quality-responsible-workers.md)</span><span class="sxs-lookup"><span data-stu-id="6bc27-133">[Configure workers who are responsible for approving nonconformances](quality-responsible-workers.md).</span></span>
1. <span data-ttu-id="6bc27-134">[ตั้งค่าคอนฟิกชนิดของปัญหา](quality-problem-types.md)</span><span class="sxs-lookup"><span data-stu-id="6bc27-134">[Configure problem types](quality-problem-types.md).</span></span>
1. <span data-ttu-id="6bc27-135">[ตั้งค่าคอนฟิกโซนตรวจสอบสินค้า](quality-quarantine-zones.md)</span><span class="sxs-lookup"><span data-stu-id="6bc27-135">[Configure quarantine zones](quality-quarantine-zones.md).</span></span>
1. <span data-ttu-id="6bc27-136">[ตั้งค่าคอนฟิกชนิดของการวินิจฉัย](quality-diagnostic-types.md)</span><span class="sxs-lookup"><span data-stu-id="6bc27-136">[Configure diagnostic types](quality-diagnostic-types.md).</span></span>
1. <span data-ttu-id="6bc27-137">[ตั้งค่าคอนฟิกการดำเนินการ](quality-operations.md)</span><span class="sxs-lookup"><span data-stu-id="6bc27-137">[Configure operations](quality-operations.md).</span></span>
1. <span data-ttu-id="6bc27-138">ไม่ระบุ: [ตั้งค่าคอนฟิกค่าธรรมเนียมคุณภาพ](quality-charges.md)</span><span class="sxs-lookup"><span data-stu-id="6bc27-138">Optional: [Configure quality charges](quality-charges.md).</span></span>

<span data-ttu-id="6bc27-139">หลังจากเสร็จสิ้นการตั้งค่าคอนฟิกแล้ว คุณสามารถเริ่มต้นสร้างและประมวลผลความไม่สอดคล้องกันได้</span><span class="sxs-lookup"><span data-stu-id="6bc27-139">After the configuration is completed, you can start to create and process nonconformances.</span></span> <span data-ttu-id="6bc27-140">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการสร้างและทำงานกับความไม่สอดคล้องกัน ให้ดูที่ [สร้างและประมวลผลความไม่สอดคล้องกัน](tasks/create-process-non-conformance.md)</span><span class="sxs-lookup"><span data-stu-id="6bc27-140">For more information about how to create and work with nonconformances, see [Create and process nonconformances](tasks/create-process-non-conformance.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6bc27-141">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="6bc27-141">Additional resources</span></span>

- [<span data-ttu-id="6bc27-142">ภาพรวมของการจัดการคุณภาพ</span><span class="sxs-lookup"><span data-stu-id="6bc27-142">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="6bc27-143">เปิดใช้งานการจัดการคุณภาพและความไม่สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="6bc27-143">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="6bc27-144">การจัดการคุณภาพสำหรับกระบวนการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="6bc27-144">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
