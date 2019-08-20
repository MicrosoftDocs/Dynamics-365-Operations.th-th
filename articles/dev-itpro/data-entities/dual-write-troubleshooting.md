---
title: คู่มือการแก้ไขปัญหาสำหรับการรวมข้อมูล
description: หัวข้อนี้แสดงข้อมูลการแก้ไขปัญหาเกี่ยวกับการรวมข้อมูลระหว่าง Microsoft Dynamics 365 for Finance and Operations และ Common Data Service
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
ms.openlocfilehash: ca62a6b3aa64ec2383ee3ded3b7bbf4650a41166
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797286"
---
# <a name="troubleshooting-guide-for-data-integration"></a><span data-ttu-id="8b20b-103">คู่มือการแก้ไขปัญหาสำหรับการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="8b20b-103">Troubleshooting guide for data integration</span></span>

## <a name="enable-plugin-trace-in-common-data-service-and-check-the-dual-write-plugin-error-details"></a><span data-ttu-id="8b20b-104">เปิดใช้งานการติดตามปลั๊กอินใน Common Data Service และตรวจสอบรายละเอียดข้อผิดพลาดปลั๊กอินการเขียนแบบคู่</span><span class="sxs-lookup"><span data-stu-id="8b20b-104">Enable Plugin Trace in Common Data Service and check the dual-write Plugin error details</span></span>

<span data-ttu-id="8b20b-105">หากคุณกำลังประสบปัญหาหรือข้อผิดพลาดกับการซิงโครไนส์การเขียนแบบคู่ คุณสามารถตรวจสอบข้อผิดพลาดในบันทึกการติดตาม:</span><span class="sxs-lookup"><span data-stu-id="8b20b-105">If you are facing an issue or error with dual-write synchronization, you can inspect the errors in the trace log:</span></span>

1. <span data-ttu-id="8b20b-106">ก่อนที่คุณจะสามารถตรวจสอบข้อผิดพลาด คุณต้องเปิดใช้งานการติดตามปลั๊กอินโดยใช้คำแนะนำใน [ลงทะเบียนปลั๊กอิน](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs) เพื่อเปิดใช้งานการติดตามปลั๊กอิน</span><span class="sxs-lookup"><span data-stu-id="8b20b-106">Before you can inspect the errors, you must enable Plugin trace using the instructions in [Register plug-in](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs) to enable Plugin trace.</span></span> <span data-ttu-id="8b20b-107">ตอนนี้คุณสามารถตรวจสอบข้อผิดพลาดได้</span><span class="sxs-lookup"><span data-stu-id="8b20b-107">Now you can inspect the errors.</span></span>
2. <span data-ttu-id="8b20b-108">ล็อกอินเข้าสู่ Dynamics 365 for Sales</span><span class="sxs-lookup"><span data-stu-id="8b20b-108">Login to Dynamics 365 for Sales.</span></span>
3. <span data-ttu-id="8b20b-109">คลิกที่ไอคอนการตั้งค่า (เกียร์) และเลือก **การตั้งค่าขั้นสูง**</span><span class="sxs-lookup"><span data-stu-id="8b20b-109">Click on the Settings icon (a gear), and select **Advanced Settings**.</span></span>
4. <span data-ttu-id="8b20b-110">ในเมนู **การตั้งค่า** เลือก **การเลือกกำหนด > ล็อกการติดตามปลั๊กอิน**</span><span class="sxs-lookup"><span data-stu-id="8b20b-110">In the **Settings** menu, choose **Customization > Plug-In Trace Log**.</span></span>
5. <span data-ttu-id="8b20b-111">คลิกที่ชื่อชนิด **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** เพื่อแสดงรายละเอียดข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="8b20b-111">Click the type name **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** to display the error details.</span></span>

## <a name="check-dual-write-synchronization-errors-in-finance-and-operations"></a><span data-ttu-id="8b20b-112">ตรวจสอบข้อผิดพลาดในการซิงโครไนส์การเขียนแบบคู่ใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8b20b-112">Check dual-write synchronization errors in Finance and Operations</span></span>

<span data-ttu-id="8b20b-113">คุณสามารถตรวจสอบข้อผิดพลาดในระหว่างการทดสอบได้โดยทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="8b20b-113">You can check the errors during testing by following these steps:</span></span>

+ <span data-ttu-id="8b20b-114">ล็อกอินเข้าสู่ LifeCycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="8b20b-114">Login to LifeCycle Services (LCS).</span></span>
+ <span data-ttu-id="8b20b-115">เปิดโครงการ LCS ที่คุณเลือกเพื่อทำการทดสอบการเขียนแบบคู่</span><span class="sxs-lookup"><span data-stu-id="8b20b-115">Open the LCS project that you chose to perform dual-write testing.</span></span>
+ <span data-ttu-id="8b20b-116">ไปยังสภาพแวดล้อมที่ใช้ Cloud</span><span class="sxs-lookup"><span data-stu-id="8b20b-116">Go to Cloud Hosted Environments.</span></span>
+ <span data-ttu-id="8b20b-117">เดสก์ท็อประยะไกลไปยัง Finance and Operations VM โดยใช้บัญชีภายในเครื่องที่แสดงใน LCS</span><span class="sxs-lookup"><span data-stu-id="8b20b-117">Remote desktop to Finance and Operations VM using local account that is displayed in LCS.</span></span>
+ <span data-ttu-id="8b20b-118">เปิดตัวแสดงเหตุการณ์</span><span class="sxs-lookup"><span data-stu-id="8b20b-118">Open the event viewer.</span></span> 
+ <span data-ttu-id="8b20b-119">นำทางไปยัง **ล็อกของแอพลิเคชันและบริการ > Microsoft > Dynamics > AX-DualWriteSync > การดำเนินงาน**</span><span class="sxs-lookup"><span data-stu-id="8b20b-119">Navigate to **Applications and Services logs > Microsoft > Dynamics > AX-DualWriteSync > Operational**.</span></span> <span data-ttu-id="8b20b-120">ข้อผิดพลาดและรายละเอียดจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="8b20b-120">The errors and details are displayed.</span></span>

## <a name="how-to-unlink-and-link-another-common-data-service-environment-from-finance-and-operations"></a><span data-ttu-id="8b20b-121">วิธียกเลิกการเชื่อมโยงและเชื่อมโยงสภาพแวดล้อม Common Data Service อื่นจาก Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8b20b-121">How to unlink and link another Common Data Service environment from Finance and Operations</span></span>

<span data-ttu-id="8b20b-122">คุณสามารถปรับปรุงการเชื่อมโยงโดยทำตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="8b20b-122">You can update links by following these steps:</span></span>

+ <span data-ttu-id="8b20b-123">นำทางไปยังสภาพแวดล้อม Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8b20b-123">Navigate to the Finance and Operations environment.</span></span>
+ <span data-ttu-id="8b20b-124">เปิดการจัดการข้อมูล</span><span class="sxs-lookup"><span data-stu-id="8b20b-124">Open Data Management.</span></span>
+ <span data-ttu-id="8b20b-125">คลิกที่ **ลิงค์ไปยัง CDS สำหรับแอป**</span><span class="sxs-lookup"><span data-stu-id="8b20b-125">Click on **Link to CDS for apps**.</span></span>
+ <span data-ttu-id="8b20b-126">เลือกการแม็ปที่กำลังรันทั้งหมด และคลิก **หยุด**</span><span class="sxs-lookup"><span data-stu-id="8b20b-126">Select all the running mappings and click **Stop**.</span></span> 
+ <span data-ttu-id="8b20b-127">เลือกการแม็ปทั้งหมด และคลิก **ลบ**</span><span class="sxs-lookup"><span data-stu-id="8b20b-127">Select all the mappings and click **Delete**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8b20b-128">ตัวเลือก **ลบ** จะไม่ปรากฏ ถ้ามีการเลือกเท็มเพลต **CustomerV3-Account**</span><span class="sxs-lookup"><span data-stu-id="8b20b-128">The **Delete** option will not appear if **CustomerV3-Account** template is selected.</span></span> <span data-ttu-id="8b20b-129">ยกเลิกการเลือก ถ้าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="8b20b-129">Unselect it if needed.</span></span> <span data-ttu-id="8b20b-130">**CustomerV3-Account** เป็นเทมเพลตที่เตรียมใช้งานที่เก่ากว่า และใช้ได้กับโซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด</span><span class="sxs-lookup"><span data-stu-id="8b20b-130">**CustomerV3-Account** is an older provisioned template and works with the Prospect to Cash solution.</span></span> <span data-ttu-id="8b20b-131">เพราะมีการนำออกใช้งานทั่วโลก ซึ่งแสดงขึ้นภายใต้เท็มเพลตทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="8b20b-131">Because it is globally released, it shows up under all templates.</span></span>

+ <span data-ttu-id="8b20b-132">คลิก **ยกเลิกการเชื่อมโยงสภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="8b20b-132">Click **Unlink environment**.</span></span>
+ <span data-ttu-id="8b20b-133">คลิก **ใช่** เพื่อยืนยัน</span><span class="sxs-lookup"><span data-stu-id="8b20b-133">Click **Yes** for confirmation.</span></span>
+ <span data-ttu-id="8b20b-134">หากต้องการเชื่อมโยงสภาพแวดล้อมใหม่ ให้ทำตามขั้นตอนใน [คู่มือการติดตั้ง](https://aka.ms/dualwrite-docs)</span><span class="sxs-lookup"><span data-stu-id="8b20b-134">To link the new environment, follow the steps in the [installation guide](https://aka.ms/dualwrite-docs).</span></span>

