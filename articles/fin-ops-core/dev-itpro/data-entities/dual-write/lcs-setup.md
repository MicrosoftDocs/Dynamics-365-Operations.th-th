---
title: การตั้งค่าการรวมแบบสองทิศทางจาก Lifecycle Services
description: หัวข้อนี้อธิบายวิธีการตั้งค่าการเชื่อมต่อการรวมแบบสองทิศทาง จาก Microsoft Dynamics Lifecycle Services (LCS)
author: RamaKrishnamoorthy
ms.date: 05/11/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: eb4170ef6cb09c862f6a4163670c519d5d8077fb
ms.sourcegitcommit: 365092f735310990e82516110141d42aaf04e654
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/27/2021
ms.locfileid: "6103580"
---
# <a name="dual-write-setup-from-lifecycle-services"></a><span data-ttu-id="d4b5b-103">การตั้งค่าการรวมแบบสองทิศทางจาก Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="d4b5b-103">Dual-write setup from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="d4b5b-104">หัวข้อนี้อธิบายวิธีการเปิดใช้งานการรวมแบบสองทิศทางจาก Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="d4b5b-104">This topic explains how to enable dual-write from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d4b5b-105">ข้อกำหนดเบื้องต้น</span><span class="sxs-lookup"><span data-stu-id="d4b5b-105">Prerequisites</span></span>

<span data-ttu-id="d4b5b-106">คุณต้องทำการรวม Power Platform ให้เสร็จสิ้นตามที่อธิบายไว้ในหัวข้อต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="d4b5b-106">You must complete the Power Platform integration as described in the following topics:</span></span>

+ [<span data-ttu-id="d4b5b-107">การรวม Power Platform - เปิดใช้งานในระหว่างการปรับใช้สภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="d4b5b-107">Power Platform Integration - Enable during environment deployment</span></span>](../../power-platform/overview.md#enable-during-environment-deployment)
+ [<span data-ttu-id="d4b5b-108">การรวม Power Platform - ตั้งค่าหลังจากการปรับใช้สภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="d4b5b-108">Power Platform integration - Set up after environment deployment</span></span>](../../power-platform/overview.md#set-up-after-environment-deployment)

## <a name="set-up-dual-write-for-new-dataverse-environments"></a><span data-ttu-id="d4b5b-109">ตั้งค่าการรวมแบบสองทิศทางสำหรับสภาพแวดล้อม Dataverse ใหม่</span><span class="sxs-lookup"><span data-stu-id="d4b5b-109">Set up dual-write for new Dataverse environments</span></span>

<span data-ttu-id="d4b5b-110">ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อตั้งค่าการรวมแบบสองทิศทางจากหน้า **รายละเอียดสภาพแวดล้อม** LCS</span><span class="sxs-lookup"><span data-stu-id="d4b5b-110">Follow these steps to set up dual-write from LCS **Environment Details** page:</span></span>

1. <span data-ttu-id="d4b5b-111">ในหน้า **รายละเอียดสภาพแวดล้อม** ให้ขยายส่วน **การรวม Power Platform**</span><span class="sxs-lookup"><span data-stu-id="d4b5b-111">On the **Environment Details** page, expand the **Power Platform Integration** section.</span></span>

2. <span data-ttu-id="d4b5b-112">เลือกปุ่ม **แอปพลิเคชันการรวมแบบสองทิศทาง**</span><span class="sxs-lookup"><span data-stu-id="d4b5b-112">Select the **Dual-write application** button.</span></span>

    ![การรวม Power Platform](media/powerplat_integration_step2.png)

3. <span data-ttu-id="d4b5b-114">ตรวจสอบข้อกำหนดและเงื่อนไข จากนั้นเลือก **กำหนดค่า**</span><span class="sxs-lookup"><span data-stu-id="d4b5b-114">Review the terms and conditions, and then select **Configure**.</span></span>

4. <span data-ttu-id="d4b5b-115">เลือก **ตกลง** เพื่อดำเนินการต่อ</span><span class="sxs-lookup"><span data-stu-id="d4b5b-115">Select **OK** to continue.</span></span>

5. <span data-ttu-id="d4b5b-116">คุณสามารถตรวจสอบความคืบหน้าโดยการรีเฟรชหน้ารายละเอียดสภาพแวดล้อมเป็นระยะๆ</span><span class="sxs-lookup"><span data-stu-id="d4b5b-116">You can monitor the progress by periodically refreshing the environment details page.</span></span> <span data-ttu-id="d4b5b-117">โดยปกติการตั้งค่าจะใช้เวลา 30 นาทีหรือน้อยกว่า</span><span class="sxs-lookup"><span data-stu-id="d4b5b-117">Setup typically takes 30 minutes or less.</span></span>  

6. <span data-ttu-id="d4b5b-118">เมื่อการตั้งค่าเสร็จสิ้น จะมีข้อความแจ้งคุณว่ากระบวนการประสบความสาเร็จหรือถ้ามีความล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="d4b5b-118">When the setup is complete, a message will inform you if the process was successful or if there was a failure.</span></span> <span data-ttu-id="d4b5b-119">ถ้าการตั้งค่าล้มเหลว จะมีข้อความแสดงข้อผิดพลาดที่เกี่ยวข้องแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="d4b5b-119">If the setup failed, then a related error message is displayed.</span></span> <span data-ttu-id="d4b5b-120">คุณต้องแก้ไขข้อผิดพลาดใด ๆ ก่อนย้ายไปยังขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="d4b5b-120">You must fix any errors before moving to the next step.</span></span>

7. <span data-ttu-id="d4b5b-121">เลือก **ลิงค์ไปยังสภาพแวดล้อม Power Platform** เพื่อสร้างลิงค์ระหว่าง Dataverse และฐานข้อมูลของสภาพแวดล้อมปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="d4b5b-121">Select **Link to Power Platform environment** to create a link between Dataverse and the current environment's databases.</span></span> <span data-ttu-id="d4b5b-122">โดยปกติขั้นตอนนี้จะใช้เวลาน้อยกว่า 5 นาที</span><span class="sxs-lookup"><span data-stu-id="d4b5b-122">This typically takes less than 5 minutes.</span></span>

    :::image type="content" source="media/powerplat_integration_step3.png" alt-text="เชื่อมโยงกับสภาพแวดล้อม Power Platform":::

8. <span data-ttu-id="d4b5b-124">เมื่อการเชื่อมโยงเสร็จสมบูรณ์ ไฮเปอร์ลิงค์จะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="d4b5b-124">When the linking is complete, a hyperlink is displayed.</span></span> <span data-ttu-id="d4b5b-125">ใช้ลิงค์เพื่อเข้าสู่ระบบพื้นที่การรวมแบบสองทิศทางในสภาพแวดล้อม Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d4b5b-125">Use the link to sign in to the dual-write administration area in the Finance and Operations environment.</span></span> <span data-ttu-id="d4b5b-126">จากที่นั่น คุณสามารถตั้งค่าการแม็ปเอนทิตีได้</span><span class="sxs-lookup"><span data-stu-id="d4b5b-126">From there, you can set up entity mappings.</span></span>

## <a name="set-up-dual-write-for-an-existing-dataverse-environment"></a><span data-ttu-id="d4b5b-127">ตั้งค่าการรวมแบบสองทิศทางสำหรับสภาพแวดล้อม Dataverse ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="d4b5b-127">Set up dual-write for an existing Dataverse environment</span></span>

<span data-ttu-id="d4b5b-128">เมื่อต้องการตั้งค่าการรวมแบบสองทิศทางให้กับสภาพแวดล้อม Dataverse ที่มีอยู่ คุณต้องสร้าง [ตั๋วสนับสนุน](../../lifecycle-services/lcs-support.md) Microsoft</span><span class="sxs-lookup"><span data-stu-id="d4b5b-128">To set up dual-write for an existing Dataverse environment, you must create a Microsoft [support ticket](../../lifecycle-services/lcs-support.md).</span></span> <span data-ttu-id="d4b5b-129">ตั๋วต้องรวม:</span><span class="sxs-lookup"><span data-stu-id="d4b5b-129">The ticket must include:</span></span>

+ <span data-ttu-id="d4b5b-130">รหัสสภาพแวดล้อม Finance and Operations ของคุณ</span><span class="sxs-lookup"><span data-stu-id="d4b5b-130">Your Finance and Operations environment ID.</span></span>
+ <span data-ttu-id="d4b5b-131">ชื่อสภาพแวดล้อมของคุณจาก Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="d4b5b-131">Your environment name from Lifecycle Services.</span></span>
+ <span data-ttu-id="d4b5b-132">รหัสองค์กร Dataverse หรือรหัสสภาพแวดล้อม Power Platform จากศูนย์การจัดการ Power Platform</span><span class="sxs-lookup"><span data-stu-id="d4b5b-132">The Dataverse organization ID or Power Platform Environment ID from Power Platform Admin Center.</span></span> <span data-ttu-id="d4b5b-133">ในตั๋วของคุณ ให้ขอรหัสเป็นอินสแตนซ์ที่ใช้ในการรวม Power Platform</span><span class="sxs-lookup"><span data-stu-id="d4b5b-133">In your ticket, request that the ID be the instance used for Power Platform integration.</span></span>

> [!NOTE]
> <span data-ttu-id="d4b5b-134">คุณไม่สามารถยกเลิกการเชื่อมโยงสภาพแวดล้อมได้โดยใช้ LCS</span><span class="sxs-lookup"><span data-stu-id="d4b5b-134">You can't unlink environments by using LCS.</span></span> <span data-ttu-id="d4b5b-135">เมื่อต้องการยกเลิกการเชื่อมโยงสภาพแวดล้อม ให้เปิดพื้นที่ทำงาน **การรวมข้อมูล** ในสภาพแวดล้อม Finance and Operations และจากนั้น เลือก **ยกเลิกการเชื่อมโยง**</span><span class="sxs-lookup"><span data-stu-id="d4b5b-135">To unlink an environment, open the **Data integration** workspace in the Finance and Operations environment, and then select **Unlink**.</span></span>

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
