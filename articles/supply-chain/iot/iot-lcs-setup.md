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
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 87d04c3df22e2d9ef56acb61e26304731a2a17a2
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206063"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a><span data-ttu-id="fd0ed-103">ติดตั้ง Add-in เครื่องมือ IoT ใน LCS</span><span class="sxs-lookup"><span data-stu-id="fd0ed-103">Install the IoT Intelligence add-in in LCS</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fd0ed-104">หัวข้อนี้อธิบายถึงวิธีการติดตั้ง Add-in เครื่องมือ IoT ใน Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="fd0ed-104">This topic explains how to install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="fd0ed-105">โปรดทราบว่า add-in ไม่สามารถติดตั้งบนสภาพแวดล้อมการสาธิต/การทดลองได้</span><span class="sxs-lookup"><span data-stu-id="fd0ed-105">Note that add-ins cannot be installed on a demo/trial environment.</span></span> <span data-ttu-id="fd0ed-106">ก่อนที่คุณจะสามารถติดตั้ง Add-in คุณต้อง [สร้างทรัพยากร Azure](iot-azure-setup.md)</span><span class="sxs-lookup"><span data-stu-id="fd0ed-106">Before you can install the add-in, you must [create the Azure resources](iot-azure-setup.md).</span></span>

## <a name="set-up-the-lcs-environment"></a><span data-ttu-id="fd0ed-107">ตั้งค่าสภาพแวดล้อม LCS</span><span class="sxs-lookup"><span data-stu-id="fd0ed-107">Set up the LCS environment</span></span>

1. <span data-ttu-id="fd0ed-108">เปิด LCS และไปที่สภาพแวดล้อม Microsoft Dynamics 365 Supply Chain Management ของคุณ</span><span class="sxs-lookup"><span data-stu-id="fd0ed-108">Open LCS, and go to your Microsoft Dynamics 365 Supply Chain Management environment.</span></span>
2. <span data-ttu-id="fd0ed-109">เลื่อนลงไปที่ส่วน **Add-in ของสภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="fd0ed-109">Scroll to the **Environment add-ins** section.</span></span>
3. <span data-ttu-id="fd0ed-110">เลือก **ติดตั้ง Add-in ใหม่** เพื่อแสดงรายการของ Add-in ที่เปิดใช้งานสำหรับสภาพแวดล้อม</span><span class="sxs-lookup"><span data-stu-id="fd0ed-110">Select **Install a new add-in** to show the list of add-ins that have been enabled for the environment.</span></span>
4. <span data-ttu-id="fd0ed-111">ในกล่องโต้ตอบ **เลือก Add-in เพื่อติดตั้ง** ให้เลือก **เครื่องมือ IoT**</span><span class="sxs-lookup"><span data-stu-id="fd0ed-111">In the **Select an add-in to install** dialog box, select **IoT Intelligence**.</span></span>
5. <span data-ttu-id="fd0ed-112">ในกล่องโต้ตอบ **ตั้งค่า Add-in** ให้ระบุรายละเอียดของฮับ IoT ของคุณและแคช Redis</span><span class="sxs-lookup"><span data-stu-id="fd0ed-112">In the **Setup add-in** dialog box, provide the details of your IoT hub and Redis cache.</span></span> <span data-ttu-id="fd0ed-113">คุณสามารถค้นหาค่าที่จำเป็นใน Key Vault ที่คุณสร้างขึ้นใน [สร้างทรัพยากร Azure](iot-azure-setup.md)</span><span class="sxs-lookup"><span data-stu-id="fd0ed-113">You can find the required values in the key vault that you created in [Create Azure resources](iot-azure-setup.md).</span></span>

    + <span data-ttu-id="fd0ed-114">**รหัสผู้เช่า** – ในพอร์ทัล Azure ให้ไปที่ Key Vault จากนั้นในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **ภาพรวม** และคัดลอกค่า **รหัสไดเรกทอรี**</span><span class="sxs-lookup"><span data-stu-id="fd0ed-114">**Tenant ID** – In the Azure portal, go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **Directory ID** value.</span></span> <span data-ttu-id="fd0ed-115">วางค่าดังกล่าวในกล่องโต้ตอบ **การตั้งค่า Add-in**</span><span class="sxs-lookup"><span data-stu-id="fd0ed-115">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="fd0ed-116">**ฮับเหตุการณ์ IoT ที่เข้ากันได้กับ Key Vault URI ของปลายทาง** – ไปที่ Key Vault จากนั้นในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **ภาพรวม** และคัดลอกค่า **ชื่อ DNS**</span><span class="sxs-lookup"><span data-stu-id="fd0ed-116">**IoT Event Hub-compatible endpoint Key Vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="fd0ed-117">วางค่าดังกล่าวในกล่องโต้ตอบ **การตั้งค่า Add-in**</span><span class="sxs-lookup"><span data-stu-id="fd0ed-117">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="fd0ed-118">**ฮับเหตุการณ์ IoT-ชื่อลับปลายทางที่เข้ากันได้** – ไปที่ Key Vault จากนั้นในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **ข้อมูลลับ** และคัดลอกชื่อข้อมูลลับที่สตริงการเชื่อมต่อฮับเหตุการณ์สำหรับฮับ IoT ถูกจัดเก็บไว้</span><span class="sxs-lookup"><span data-stu-id="fd0ed-118">**IoT Event Hub-compatible endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the event hub connection string for the IoT hub is stored.</span></span> <span data-ttu-id="fd0ed-119">วางค่าดังกล่าวในกล่องโต้ตอบ **การตั้งค่า Add-in**</span><span class="sxs-lookup"><span data-stu-id="fd0ed-119">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="fd0ed-120">**URI ของ Key Vault แคช Redis** – ไปที่ Key Vault จากนั้นในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **ภาพรวม** และคัดลอกค่า **ชื่อ DNS**</span><span class="sxs-lookup"><span data-stu-id="fd0ed-120">**Redis cache key vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="fd0ed-121">วางค่าดังกล่าวในกล่องโต้ตอบ **การตั้งค่า Add-in**</span><span class="sxs-lookup"><span data-stu-id="fd0ed-121">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="fd0ed-122">**ชื่อข้อมูลลับปลายทางแคช Redis** – ไปที่ Key Vault จากนั้นในบานหน้าต่างนำทางด้านซ้าย ให้เลือก **ข้อมูลลับ** และคัดลอกชื่อข้อมูลลับที่สตริงการเชื่อมต่อฮับสำหรับแคช Redis ถูกจัดเก็บไว้</span><span class="sxs-lookup"><span data-stu-id="fd0ed-122">**Redis cache endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the connection string for the Redis cache is stored.</span></span> <span data-ttu-id="fd0ed-123">วางค่าดังกล่าวในกล่องโต้ตอบ **การตั้งค่า Add-in**</span><span class="sxs-lookup"><span data-stu-id="fd0ed-123">Paste that value in the **Setup add-in** dialog box.</span></span>

6. <span data-ttu-id="fd0ed-124">เลือกกล่องกาเครื่องหมายเพื่อยอมรับข้อกำหนดและเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="fd0ed-124">Select the check box to accept the terms and conditions.</span></span>
7. <span data-ttu-id="fd0ed-125">เลือก **ติดตั้ง**</span><span class="sxs-lookup"><span data-stu-id="fd0ed-125">Select **Install**.</span></span>
8. <span data-ttu-id="fd0ed-126">กล่องข้อความจะปรากฏขึ้นโดยระบุว่า "Add-in ถูกทริกเกอร์สำหรับการติดตั้งเสร็จเรียบร้อยแล้ว"</span><span class="sxs-lookup"><span data-stu-id="fd0ed-126">A message box appears that states, "Add-in has been successfully triggered for installation."</span></span> <span data-ttu-id="fd0ed-127">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="fd0ed-127">Select **OK**.</span></span>

<span data-ttu-id="fd0ed-128">ขณะนี้การตั้งค่า LCS เสร็จสมบูรณ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="fd0ed-128">LCS setup is now completed.</span></span> <span data-ttu-id="fd0ed-129">ขั้นตอนต่อไปคือ [ตั้งค่าสถานการณ์จำลอง](iot-scenario-setup.md)</span><span class="sxs-lookup"><span data-stu-id="fd0ed-129">The next step is to [set up the scenarios](iot-scenario-setup.md).</span></span>

## <a name="uninstall-the-add-in"></a><a id="uninstall-addin"></a><span data-ttu-id="fd0ed-130">ถอนการติดตั้ง Add-in</span><span class="sxs-lookup"><span data-stu-id="fd0ed-130">Uninstall the add-in</span></span>

1. <span data-ttu-id="fd0ed-131">ใน Supply Chain Management [ปิดใช้งานสถานการณ์จำลอง](iot-scenario-setup.md#disable-a-scenario)</span><span class="sxs-lookup"><span data-stu-id="fd0ed-131">In Supply Chain Management, [disable the scenarios](iot-scenario-setup.md#disable-a-scenario).</span></span>
2. <span data-ttu-id="fd0ed-132">ใน LCS ไปยังรายละเอียดสภาพแวดล้อม Supply Chain Management ของคุณ</span><span class="sxs-lookup"><span data-stu-id="fd0ed-132">In LCS, go to your Supply Chain Management environment details.</span></span>
3. <span data-ttu-id="fd0ed-133">เลื่อนลงไปที่ส่วน **Add-in ของสภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="fd0ed-133">Scroll to the **Environment add-ins** section.</span></span>
4. <span data-ttu-id="fd0ed-134">เลือก **ถอนการติดตั้ง** สำหรับ Add-in ครื่องมือ IoT</span><span class="sxs-lookup"><span data-stu-id="fd0ed-134">Select **Uninstall** for the IoT Intelligence add-in.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]