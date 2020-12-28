---
title: ติดตั้ง Add-in เครื่องมือ IoT ใน LCS
description: หัวข้อนี้อธิบายถึงวิธีการติดตั้ง Add-in เครื่องมือ IoT ใน Microsoft Dynamics Lifecycle Services (LCS)
author: robinarh
manager: tfehr
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ad8b33633646f27bc368dc4bbedc1eb64c150a9f
ms.sourcegitcommit: 092ef6a45f515b38be2a4481abdbe7518a636f85
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/16/2020
ms.locfileid: "4438795"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a><span data-ttu-id="974b6-103">ติดตั้ง Add-in เครื่องมือ IoT ใน LCS</span><span class="sxs-lookup"><span data-stu-id="974b6-103">Install the IoT Intelligence add-in in LCS</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="974b6-104">หัวข้อนี้อธิบายถึงวิธีการติดตั้ง Add-in เครื่องมือ IoT ใน Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="974b6-104">This topic explains how to install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="974b6-105">โปรดทราบว่า add-in ไม่สามารถติดตั้งบนสภาพแวดล้อมการสาธิต/การทดลองได้</span><span class="sxs-lookup"><span data-stu-id="974b6-105">Note that add-ins cannot be installed on a demo/trial environment.</span></span> <span data-ttu-id="974b6-106">ก่อนที่คุณจะสามารถติดตั้ง Add-in คุณต้อง [สร้างทรัพยากร Azure](iot-azure-setup.md)</span><span class="sxs-lookup"><span data-stu-id="974b6-106">Before you can install the add-in, you must [create the Azure resources](iot-azure-setup.md).</span></span>

## <a name="set-up-the-lcs-environment"></a><span data-ttu-id="974b6-107">ตั้งค่าสภาพแวดล้อม LCS</span><span class="sxs-lookup"><span data-stu-id="974b6-107">Set up the LCS environment</span></span>

1. <span data-ttu-id="974b6-108">เปิด LCS และไปที่สภาพแวดล้อม Microsoft Dynamics 365 Supply Chain Management ของคุณ</span><span class="sxs-lookup"><span data-stu-id="974b6-108">Open LCS, and go to your Microsoft Dynamics 365 Supply Chain Management environment.</span></span>
2. <span data-ttu-id="974b6-109">เลื่อนลงไปที่ส่วน **Add-in ของสภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="974b6-109">Scroll to the **Environment add-ins** section.</span></span>
3. <span data-ttu-id="974b6-110">เลือก **ติดตั้ง Add-in ใหม่** เพื่อแสดงรายการของ Add-in ที่เปิดใช้งานสำหรับสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="974b6-110">Select **Install a new add-in** to show the list of add-ins that have been enabled for the environment.</span></span>
4. <span data-ttu-id="974b6-111">ในกล่องโต้ตอบ **เลือก Add-in เพื่อติดตั้ง** ให้เลือก **เครื่องมือ IoT**</span><span class="sxs-lookup"><span data-stu-id="974b6-111">In the **Select an add-in to install** dialog box, select **IoT Intelligence**.</span></span>
5. <span data-ttu-id="974b6-112">ในกล่องโต้ตอบ **ตั้งค่า Add-in** ให้ระบุรายละเอียดของฮับ IoT ของคุณและแคช Redis</span><span class="sxs-lookup"><span data-stu-id="974b6-112">In the **Setup add-in** dialog box, provide the details of your IoT hub and Redis cache.</span></span> <span data-ttu-id="974b6-113">คุณสามารถค้นหาค่าที่จำเป็นใน Key Vault ที่คุณสร้างขึ้นใน [สร้างทรัพยากร Azure](iot-azure-setup.md)</span><span class="sxs-lookup"><span data-stu-id="974b6-113">You can find the required values in the key vault that you created in [Create Azure resources](iot-azure-setup.md).</span></span>

    + <span data-ttu-id="974b6-114">**รหัสผู้เช่า** – ในพอร์ทัล Azure ให้ไปที่ Key Vault จากนั้นในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **ภาพรวม** และคัดลอกค่า **รหัสไดเรกทอรี**</span><span class="sxs-lookup"><span data-stu-id="974b6-114">**Tenant ID** – In the Azure portal, go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **Directory ID** value.</span></span> <span data-ttu-id="974b6-115">วางค่าดังกล่าวในกล่องโต้ตอบ **การตั้งค่า Add-in**</span><span class="sxs-lookup"><span data-stu-id="974b6-115">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="974b6-116">**ฮับเหตุการณ์ IoT ที่เข้ากันได้กับ Key Vault URI ของปลายทาง** – ไปที่ Key Vault จากนั้นในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **ภาพรวม** และคัดลอกค่า **ชื่อ DNS**</span><span class="sxs-lookup"><span data-stu-id="974b6-116">**IoT Event Hub-compatible endpoint Key Vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="974b6-117">วางค่าดังกล่าวในกล่องโต้ตอบ **การตั้งค่า Add-in**</span><span class="sxs-lookup"><span data-stu-id="974b6-117">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="974b6-118">**ฮับเหตุการณ์ IoT-ชื่อลับปลายทางที่เข้ากันได้** – ไปที่ Key Vault จากนั้นในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **ข้อมูลลับ** และคัดลอกชื่อข้อมูลลับที่สตริงการเชื่อมต่อฮับเหตุการณ์สำหรับฮับ IoT ถูกจัดเก็บไว้</span><span class="sxs-lookup"><span data-stu-id="974b6-118">**IoT Event Hub-compatible endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the event hub connection string for the IoT hub is stored.</span></span> <span data-ttu-id="974b6-119">วางค่าดังกล่าวในกล่องโต้ตอบ **การตั้งค่า Add-in**</span><span class="sxs-lookup"><span data-stu-id="974b6-119">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="974b6-120">**URI ของ Key Vault แคช Redis** – ไปที่ Key Vault จากนั้นในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **ภาพรวม** และคัดลอกค่า **ชื่อ DNS**</span><span class="sxs-lookup"><span data-stu-id="974b6-120">**Redis cache key vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="974b6-121">วางค่าดังกล่าวในกล่องโต้ตอบ **การตั้งค่า Add-in**</span><span class="sxs-lookup"><span data-stu-id="974b6-121">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="974b6-122">**ชื่อข้อมูลลับปลายทางแคช Redis** – ไปที่ Key Vault จากนั้นในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **ข้อมูลลับ** และคัดลอกชื่อข้อมูลลับที่สตริงการเชื่อมต่อฮับสำหรับแคช Redis ถูกจัดเก็บไว้</span><span class="sxs-lookup"><span data-stu-id="974b6-122">**Redis cache endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the connection string for the Redis cache is stored.</span></span> <span data-ttu-id="974b6-123">วางค่าดังกล่าวในกล่องโต้ตอบ **การตั้งค่า Add-in**</span><span class="sxs-lookup"><span data-stu-id="974b6-123">Paste that value in the **Setup add-in** dialog box.</span></span>

6. <span data-ttu-id="974b6-124">เลือกกล่องกาเครื่องหมายเพื่อยอมรับข้อกำหนดและเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="974b6-124">Select the check box to accept the terms and conditions.</span></span>
7. <span data-ttu-id="974b6-125">เลือก **ติดตั้ง**</span><span class="sxs-lookup"><span data-stu-id="974b6-125">Select **Install**.</span></span>
8. <span data-ttu-id="974b6-126">กล่องข้อความจะปรากฏขึ้นโดยระบุว่า "Add-in ถูกทริกเกอร์สำหรับการติดตั้งเสร็จเรียบร้อยแล้ว"</span><span class="sxs-lookup"><span data-stu-id="974b6-126">A message box appears that states, "Add-in has been successfully triggered for installation."</span></span> <span data-ttu-id="974b6-127">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="974b6-127">Select **OK**.</span></span>

<span data-ttu-id="974b6-128">ขณะนี้การตั้งค่า LCS เสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="974b6-128">LCS setup is now completed.</span></span> <span data-ttu-id="974b6-129">ขั้นตอนต่อไปคือ [ตั้งค่าสถานการณ์จำลอง](iot-scenario-setup.md)</span><span class="sxs-lookup"><span data-stu-id="974b6-129">The next step is to [set up the scenarios](iot-scenario-setup.md).</span></span>

## <a name="uninstall-the-add-in"></a><a id="uninstall-addin"></a><span data-ttu-id="974b6-130">ถอนการติดตั้ง Add-in</span><span class="sxs-lookup"><span data-stu-id="974b6-130">Uninstall the add-in</span></span>

1. <span data-ttu-id="974b6-131">ใน Supply Chain Management [ปิดใช้งานสถานการณ์จำลอง](iot-scenario-setup.md#disable-a-scenario)</span><span class="sxs-lookup"><span data-stu-id="974b6-131">In Supply Chain Management, [disable the scenarios](iot-scenario-setup.md#disable-a-scenario).</span></span>
2. <span data-ttu-id="974b6-132">ใน LCS ไปยังรายละเอียดสภาพแวดล้อม Supply Chain Management ของคุณ</span><span class="sxs-lookup"><span data-stu-id="974b6-132">In LCS, go to your Supply Chain Management environment details.</span></span>
3. <span data-ttu-id="974b6-133">เลื่อนลงไปที่ส่วน **Add-in ของสภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="974b6-133">Scroll to the **Environment add-ins** section.</span></span>
4. <span data-ttu-id="974b6-134">เลือก **ถอนการติดตั้ง** สำหรับ Add-in ครื่องมือ IoT</span><span class="sxs-lookup"><span data-stu-id="974b6-134">Select **Uninstall** for the IoT Intelligence add-in.</span></span>
