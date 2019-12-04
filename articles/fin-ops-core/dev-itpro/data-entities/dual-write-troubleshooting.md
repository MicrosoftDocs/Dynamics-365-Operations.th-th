---
title: คู่มือการแก้ไขปัญหาสำหรับการรวมข้อมูล
description: หัวข้อนี้แสดงข้อมูลการแก้ไขปัญหาสำหรับการรวมข้อมูลระหว่างแอพลิเคชัน Finance and Operations และ Common Data Service
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 35c0a1e6342008bc2ee6ff25a1663e199c8cb985
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771036"
---
# <a name="troubleshooting-guide-for-data-integration"></a><span data-ttu-id="c9751-103">คู่มือการแก้ไขปัญหาสำหรับการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="c9751-103">Troubleshooting guide for data integration</span></span>

## <a name="enable-plug-in-trace-logs-in-common-data-service-and-inspect-the-dual-write-plug-in-error-details"></a><span data-ttu-id="c9751-104">เปิดใช้ล็อกการติดตามปลั๊กอินใน Common Data Service และตรวจสอบรายละเอียดข้อผิดพลาดปลั๊กอินการเขียนแบบคู่</span><span class="sxs-lookup"><span data-stu-id="c9751-104">Enable plug-in trace logs in Common Data Service and inspect the dual-write plug-in error details</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c9751-105">ถ้าคุณพบปัญหาหรือข้อผิดพลาดระหว่างการซิงโครไนส์การเขียนแบบคู่ ให้ทำตามขั้นตอนต่อไปนี้เพื่อตรวจสอบข้อผิดพลาดในล็อกการติดตาม</span><span class="sxs-lookup"><span data-stu-id="c9751-105">If you experience an issue or error during dual-write synchronization, follow these steps to inspect the errors in the trace log.</span></span>

1. <span data-ttu-id="c9751-106">ก่อนที่คุณจะสามารถตรวจสอบข้อผิดพลาดได้ คุณต้องเปิดใช้งานล็อกการติดตามปลั๊กอิน</span><span class="sxs-lookup"><span data-stu-id="c9751-106">Before you can inspect the errors, you must enable plug-in trace logs.</span></span> <span data-ttu-id="c9751-107">สำหรับคำแนะนำ ให้ดูที่ส่วน "ดูล็อกการติดตาม" ของ [บทช่วยสอน: เขียนและลงทะเบียนปลั๊กอิน](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs)</span><span class="sxs-lookup"><span data-stu-id="c9751-107">For instructions, see the "View trace logs" section of [Tutorial: Write and register a plug-in](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs).</span></span>

    <span data-ttu-id="c9751-108">ตอนนี้คุณสามารถตรวจสอบข้อผิดพลาดได้</span><span class="sxs-lookup"><span data-stu-id="c9751-108">You can now inspect the errors.</span></span>

2. <span data-ttu-id="c9751-109">ลงชื่อเข้าใช้ Microsoft Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="c9751-109">Sign in to Microsoft Dynamics 365 Sales.</span></span>
3. <span data-ttu-id="c9751-110">เลือกปุ่ม **การตั้งค่า** (สัญลักษณ์เกียร์) แล้วจากนั้น เลือก **การตั้งค่าขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="c9751-110">Select the **Settings** button (the gear symbol), and then select **Advanced Settings**.</span></span>
4. <span data-ttu-id="c9751-111">ในเมนู **การตั้งค่า** เลือก **การเลือกกำหนด \> ล็อกการติดตามปลั๊กอิน**</span><span class="sxs-lookup"><span data-stu-id="c9751-111">On the **Settings** menu, select **Customization \> Plug-In Trace Log**.</span></span>
5. <span data-ttu-id="c9751-112">เลือก **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** เป็นชื่อชนิด เพื่อแสดงรายละเอียดข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="c9751-112">Select **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** as the type name to show the error details.</span></span>

## <a name="inspect-dual-write-synchronization-errors"></a><span data-ttu-id="c9751-113">ตรวจสอบข้อผิดพลาดของการซิงโครไนส์การเขียนแบบสองครั้ง</span><span class="sxs-lookup"><span data-stu-id="c9751-113">Inspect dual-write synchronization errors</span></span>

<span data-ttu-id="c9751-114">ทำตามขั้นตอนต่อไปนี้เพื่อตรวจสอบข้อผิดพลาดในระหว่างการทดสอบ</span><span class="sxs-lookup"><span data-stu-id="c9751-114">Follow these steps to inspect errors during testing.</span></span>

1. <span data-ttu-id="c9751-115">ลงชื่อเข้าใช้ Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="c9751-115">Sign in to Microsoft Dynamics Lifecycle Services (LCS).</span></span>
2. <span data-ttu-id="c9751-116">เปิดโครงการ LCS เพื่อทำการทดสอบการเขียนแบบคู่</span><span class="sxs-lookup"><span data-stu-id="c9751-116">Open the LCS project to do dual-write testing for.</span></span>
3. <span data-ttu-id="c9751-117">เลือก **สภาพแวดล้อมที่โฮสต์ระบบคลาวด์**</span><span class="sxs-lookup"><span data-stu-id="c9751-117">Select **Cloud-hosted environments**.</span></span>
4. <span data-ttu-id="c9751-118">ทำการเชื่อมต่อเดสก์ท็อประยะไกลกับแอพลิเคชั่นเครื่องเสมือน (VM) โดยใช้บัญชีภายในเครื่องที่แสดงอยู่ใน LCS</span><span class="sxs-lookup"><span data-stu-id="c9751-118">Make a Remote desktop connection to the application virtual machine (VM) by using local account that is shown in LCS.</span></span>
5. <span data-ttu-id="c9751-119">เปิดตัวแสดงเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="c9751-119">Open Event Viewer.</span></span> 
6. <span data-ttu-id="c9751-120">ไปยัง **ล็อกของแอพลิเคชันและบริการ \> Microsoft \> Dynamics \> AX-DualWriteSync \> การดำเนินงาน**</span><span class="sxs-lookup"><span data-stu-id="c9751-120">Go to **Applications and Services Logs \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operational**.</span></span> <span data-ttu-id="c9751-121">ข้อผิดพลาดและรายละเอียดจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="c9751-121">The errors and details are shown.</span></span>

## <a name="unlink-one-common-data-service-environment-from-the-application-and-link-another-environment"></a><span data-ttu-id="c9751-122">ยกเลิกการเชื่อมโยงสภาพแวดล้อม Common Data Service หนึ่งรายการจากแอพลิเคชันและเชื่อมโยงสภาพแวดล้อมอื่น</span><span class="sxs-lookup"><span data-stu-id="c9751-122">Unlink one Common Data Service environment from the application and link another environment</span></span>

<span data-ttu-id="c9751-123">ทำตามขั้นตอนเหล่านี้เพื่อปรับปรุงการเชื่อมโยง</span><span class="sxs-lookup"><span data-stu-id="c9751-123">Follow these steps to update links.</span></span>

1. <span data-ttu-id="c9751-124">ไปที่ สภาพแวดล้องแอพลิเคชัน</span><span class="sxs-lookup"><span data-stu-id="c9751-124">Go to the application environment.</span></span>
2. <span data-ttu-id="c9751-125">เปิดการจัดการข้อมูล</span><span class="sxs-lookup"><span data-stu-id="c9751-125">Open Data Management.</span></span>
3. <span data-ttu-id="c9751-126">เลือก **ลิงค์ไปยัง CDS สำหรับแอป**</span><span class="sxs-lookup"><span data-stu-id="c9751-126">Select **Link to CDS for apps**.</span></span>
4. <span data-ttu-id="c9751-127">เลือกการแม็ปทั้งหมดที่กำลังรัน แล้วจากนั้น เลือก **หยุด**</span><span class="sxs-lookup"><span data-stu-id="c9751-127">Select all the mappings that are running, and then select **Stop**.</span></span>
5. <span data-ttu-id="c9751-128">เลือกการแม็ปทั้งหมด และจากนั้น เลือก **ลบ**</span><span class="sxs-lookup"><span data-stu-id="c9751-128">Select all the mappings, and then select **Delete**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c9751-129">ตัวเลือก **ลบ** จะไม่พร้อมใช้งาน ถ้ามีการเลือกเท็มเพลต **CustomerV3-Account**</span><span class="sxs-lookup"><span data-stu-id="c9751-129">The **Delete** option isn't available if the **CustomerV3-Account** template is selected.</span></span> <span data-ttu-id="c9751-130">ยกเลิกการเลือกเท็มเพลตนี้ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="c9751-130">Clear the selection of this template as required.</span></span> <span data-ttu-id="c9751-131">**CustomerV3-Account** เป็นเทมเพลตที่เตรียมใช้งานที่เก่ากว่า และใช้ได้กับโซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด</span><span class="sxs-lookup"><span data-stu-id="c9751-131">**CustomerV3-Account** is an older provisioned template and works with the Prospect to Cash solution.</span></span> <span data-ttu-id="c9751-132">เพราะมีการนำออกใช้งานทั่วโลก ซึ่งแสดงขึ้นภายใต้เท็มเพลตทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="c9751-132">Because it's globally released, it appears under all templates.</span></span>

6. <span data-ttu-id="c9751-133">เลือก **ยกเลิกการเชื่อมโยงสภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="c9751-133">Select **Unlink environment**.</span></span>
7. <span data-ttu-id="c9751-134">เลือก **ใช่** เพื่อยืนยันการดำเนินงาน</span><span class="sxs-lookup"><span data-stu-id="c9751-134">Select **Yes** to confirm the operation.</span></span>
8. <span data-ttu-id="c9751-135">หากต้องการเชื่อมโยงสภาพแวดล้อมใหม่ ให้ทำตามขั้นตอนใน [คู่มือการติดตั้ง](https://aka.ms/dualwrite-docs)</span><span class="sxs-lookup"><span data-stu-id="c9751-135">To link the new environment, follow the steps in the [installation guide](https://aka.ms/dualwrite-docs).</span></span>
