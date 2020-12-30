---
title: เปิดใช้งานการคาดคะเนการชำระเงินของลูกค้า (ตัวอย่าง)
description: หัวข้อนี้จะอธิบายวิธีการเปิดและตั้งค่าคอนฟิกลักษณะการทำงานการคาดการณ์การชำระเงินของลูกค้าในข้อมูลเชิงลึกทางการเงิน
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: e10aa9342ec9f089ef8ecec5e1221a31c580fc87
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645004"
---
# <a name="enable-customer-payment-predictions-preview"></a><span data-ttu-id="6f011-103">เปิดใช้งานการคาดคะเนการชำระเงินของลูกค้า (ตัวอย่าง)</span><span class="sxs-lookup"><span data-stu-id="6f011-103">Enable customer payment predictions (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="6f011-104">หัวข้อนี้จะอธิบายวิธีการเปิดและตั้งค่าคอนฟิกลักษณะการทำงานการคาดการณ์การชำระเงินของลูกค้าในข้อมูลเชิงลึกทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="6f011-104">This topic explains how to turn on and configure the Customer payment predictions feature in Finance insights.</span></span> <span data-ttu-id="6f011-105">คุณเปิดใช้งานลักษณะการทำงานในพื้นที่ทำงาน **การจัดการลักษณะการทำงาน** และป้อนการตั้งค่าการตั้งค่าคอนฟิกในหน้า **พารามิเตอร์ข้อมูลเชิงลึกทางการเงิน**</span><span class="sxs-lookup"><span data-stu-id="6f011-105">You turn on the feature in the **Feature management** workspace and enter configuration settings on the **Financial insights parameters** page.</span></span> <span data-ttu-id="6f011-106">หัวข้อนี้ยังมีข้อมูลที่ช่วยให้คุณสามารถใช้ลักษณะการทำงานได้อย่างมีประสิทธิภาพ</span><span class="sxs-lookup"><span data-stu-id="6f011-106">This topic also includes information that can help you effectively use the feature.</span></span>

> [!NOTE]
> <span data-ttu-id="6f011-107">ก่อนที่คุณจะดำเนินการตามขั้นตอนต่อไปนี้ ให้ตรวจสอบให้แน่ใจว่าได้ดำเนินการขั้นตอนที่จำเป็นใน [ตั้งค่าคอนฟิกสำหรับหัวข้อข้อมูลเชิงลึก](configure-for-fin-insites.md)</span><span class="sxs-lookup"><span data-stu-id="6f011-107">Before you complete the following steps, be sure to complete the prerequisite steps in the [Configure for Finance insights](configure-for-fin-insites.md) topic.</span></span>

1. <span data-ttu-id="6f011-108">ใช้ข้อมูลจากหน้าสภาพแวดล้อมใน Microsoft Dynamics Lifecycle Services (LCS) เพื่อเชื่อมต่อกับอินสแตนซ์หลักของ AZURE SQL สำหรับสภาพแวดล้อมดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="6f011-108">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="6f011-109">รันคำสั่ง Transact-SQL (T-SQL) ต่อไปนี้เพื่อเปิดใช้งานเที่ยวบินสำหรับสภาพแวดล้อม sandbox</span><span class="sxs-lookup"><span data-stu-id="6f011-109">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="6f011-110">(คุณอาจต้องเปิดใช้งานการเข้าถึงสำหรับที่อยู่ IP ของคุณใน LCS ก่อนที่คุณจะสามารถเชื่อมต่อระยะไกลกับเซิร์ฟเวอออบเจ็กต์โปรแกรมประยุกต์ \[AOS\])</span><span class="sxs-lookup"><span data-stu-id="6f011-110">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED, PARTITION) VALUES ('PayPredEnableFeature', 1, 5637144576)`

    > [!NOTE]
    > <span data-ttu-id="6f011-111">ถ้าการปรับใช้ Microsoft Dynamics 365 Finance ของคุณเป็นการปรับใช้การให้บริการ คุณสามารถข้ามขั้นตอนนี้ได้</span><span class="sxs-lookup"><span data-stu-id="6f011-111">If your deployment of Microsoft Dynamics 365 Finance is a Service Fabric deployment, you can skip this step.</span></span> <span data-ttu-id="6f011-112">ทีมงานในเชิงลึกของการเงินควรมีการเปิดใช้งานเที่ยวบินให้คุณแล้ว</span><span class="sxs-lookup"><span data-stu-id="6f011-112">The Finance insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="6f011-113">ถ้าคุณไม่เห็นคุณลักษณะในพื้นที่ทำงาน **การจัดการลักษณะการทำงาน** หรือหากประสบปัญหาเมื่อคุณพยายามเปิดใช้งาน โปรดติดต่อ <fiap@microsoft.com></span><span class="sxs-lookup"><span data-stu-id="6f011-113">If you don't see the feature in the **Feature management** workspace, or if experience issues when you try to turn it on, contact <fiap@microsoft.com>.</span></span>

2. <span data-ttu-id="6f011-114">เปิดลักษณะการทำงานข้อมูลเชิงลึกของการชำระเงินของลูกค้า:</span><span class="sxs-lookup"><span data-stu-id="6f011-114">Turn on the Customer payment insights feature:</span></span>

    1. <span data-ttu-id="6f011-115">ไปที่ **การดูแลระบบ \> พื้นที่ทำงาน \> การจัดการคุณลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="6f011-115">Go to **System administration \> Workspaces \> Feature management**.</span></span>
    2. <span data-ttu-id="6f011-116">ค้นหาลักษณะการทำงานที่ชื่อ **ข้อมูลเชิงลึกของการชำระเงินของลูกค้า (ตัวอย่าง)**</span><span class="sxs-lookup"><span data-stu-id="6f011-116">Find the feature that is named **Customer payment insights (preview)**.</span></span>
    3. <span data-ttu-id="6f011-117">เลือก **เปิดใช้งาน**</span><span class="sxs-lookup"><span data-stu-id="6f011-117">Select **Enable now**.</span></span>

    <span data-ttu-id="6f011-118">ขณะนี้มีการเปิดใช้งานลักษณะการทำงานในเชิงลึกของการชำระเงินของลูกค้าและพร้อมที่จะตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="6f011-118">The Customer payment insights feature is now turned on and ready to be configured.</span></span>

3. <span data-ttu-id="6f011-119">ตั้งค่าคอนฟิกข้อมูลเชิงลึกของการชำระเงินของลูกค้า:</span><span class="sxs-lookup"><span data-stu-id="6f011-119">Configure the Customer payment insights feature:</span></span>

    1. <span data-ttu-id="6f011-120">ไปที่ **เครดิตและการเรียกเก็บเงินข้อมูลเชิงลึก \> การตั้งค่า \> ข้อมูลเชิงลึกทางการเงิน \> พารามิเตอร์ข้อมูลเชิงลึกทางการเงิน**</span><span class="sxs-lookup"><span data-stu-id="6f011-120">Go to **Credit and collections \> Setup \> Finance insights \> Finance insights parameters**.</span></span>

        <span data-ttu-id="6f011-121">[![หน้าพารามิเตอร์ข้อมูลเชิงลึกทางการเงินก่อนที่จะมีการตั้งค่าคอนฟิกลักษณะการทำงาน](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)</span><span class="sxs-lookup"><span data-stu-id="6f011-121">[![Financial insights parameters page before the feature is configured](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)</span></span>

    2. <span data-ttu-id="6f011-122">บนหน้า **พารามิเตอร์ข้อมูลเชิงลึกทางการเงิน** บนแท็บ **ข้อมูลเชิงลึกของการชำระเงินของลูกค้า** ให้เลือกลิงค์ **ดูฟิลด์ข้อมูลที่ใช้ในแบบจำลองการคาดคะเน** เพื่อเปิดหน้า **ฟิลด์ข้อมูลสำหรับแบบจำลองการคาดคะเน**</span><span class="sxs-lookup"><span data-stu-id="6f011-122">On the **Financial insights parameters** page, on the **Customer payment insights** tab, select the **View the data fields used in the prediction model** link to open the **Data fields for prediction model** page.</span></span> <span data-ttu-id="6f011-123">คุณสามารถดูรายการเริ่มต้นของฟิลด์ที่ใช้ในการสร้างแบบจำลองการคาดคะเนปัญญาประดิษฐ์ (AI) สำหรับการคาดการณ์การชำระเงินของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="6f011-123">There, you can view the default list of fields that are used to create the artificial intelligence (AI) prediction model for customer payment predictions.</span></span>

        <span data-ttu-id="6f011-124">เมื่อต้องการใช้รายการเริ่มต้นของฟิลด์เพื่อสร้างแบบจำลองการคาดคะเน ให้ปิดหน้า **ฟิลด์ข้อมูลสำหรับแบบจำลองการคาดคะเน** จากนั้นบนหน้า **พารามิเตอร์ข้อมูลเชิงลึกทางการเงิน** ตั้งค่าตัวเลือก **เปิดใช้งานลักษณะการทำงาน** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="6f011-124">To use the default list of fields to create the prediction model, close the **Data fields for prediction model** page, and then, on the **Financial insights parameters** page, set the **Enable feature** option to **Yes**.</span></span>

    3. <span data-ttu-id="6f011-125">ระบุรอบระยะเวลาธุรกรรม "ล่าช้ามาก" เพื่อกำหนดว่าบักเก็ตการคาดคะเน **ล่าช้ามาก** เป็นอย่างไรสำหรับธุรกิจของคุณ</span><span class="sxs-lookup"><span data-stu-id="6f011-125">Specify the "very late" transaction period to define what the **Very late** prediction bucket means for your business.</span></span>

        <span data-ttu-id="6f011-126">สำหรับแต่ละใบแจ้งหนี้ที่เปิดค้างไว้ระบบจะทำนายความน่าจะเป็นของการชำระเงินในสามบักเก็ต: **ในเวลา** **ล่าช้า** และ **ล่าช้ามาก**</span><span class="sxs-lookup"><span data-stu-id="6f011-126">For each open invoice, the system predicts the probability of payment in three buckets: **On time**, **Late**, and **Very late**.</span></span>

        - <span data-ttu-id="6f011-127">**ในเวลา** – บักเก็ตนี้รวมถึงการชำระเงินที่คาดการณ์ไว้สำหรับการชำระเงินในหรือก่อนวันที่ครบกำหนดของธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="6f011-127">**On time** – This bucket includes payments that are predicted to be paid on or before the transaction due date.</span></span>
        - <span data-ttu-id="6f011-128">**ล่าช้า** – บักเก็ตนี้รวมถึงการชำระเงินที่คาดการณ์ไว้หลังจากวันครบกำหนดของธุรกรรมแต่ก่อนเริ่มต้นรอบระยะเวลาธุรกรรม "ล่าช้า"</span><span class="sxs-lookup"><span data-stu-id="6f011-128">**Late** – This bucket includes payments that are predicted to be paid after the transaction due date but before the start of the "very late" transaction period.</span></span>
        - <span data-ttu-id="6f011-129">**ล่าช้ามาก** – บักเก็ตนี้รวมถึงการชำระเงินที่คาดการณ์ไว้หลังจากวันครบรอบระยะเวลาธุรกรรม "ล่าช้ามาก"</span><span class="sxs-lookup"><span data-stu-id="6f011-129">**Very late** – This bucket includes payments that are predicted to be paid after the start of the "very late" transaction period.</span></span>

        > [!NOTE]
        > <span data-ttu-id="6f011-130">ถ้าคุณเปลี่ยนรอบระยะเวลาของธุรกรรม "ล่าช้ามาก" และเลือก **เปลี่ยนขีดจำกัดล่าช้า** หลังจากที่มีการสร้างแบบจำลองการคาดคะเน AI สำหรับการชำระเงินของลูกค้า แบบจำลองการคาดการณ์ที่มีอยู่จะถูกลบออกและสร้างแบบจำลองใหม่</span><span class="sxs-lookup"><span data-stu-id="6f011-130">If you change the "very late" transaction period and select **Change late threshold** after the AI prediction model for customer payments has been created, the existing prediction model is deleted, and a new model is created.</span></span> <span data-ttu-id="6f011-131">แบบจำลองการคาดคะเนใหม่จะย้ายธุรกรรมไปยังรอบระยะเวลา "ล่าช้ามาก" ตามการตั้งค่าที่ป้อนไว้เพื่อกำหนด</span><span class="sxs-lookup"><span data-stu-id="6f011-131">The new prediction model will move transactions into the "very late" period, based on the settings that were entered to define it.</span></span>

    4. <span data-ttu-id="6f011-132">หลังจากที่คุณได้กำหนดรอบระยะเวลาของธุรกรรม "ล่าช้ามาก" แล้ว ให้เลือก **สร้างแบบจำลองการคาดคะเน** เพื่อสร้างแบบจำลองการคาดคะเน</span><span class="sxs-lookup"><span data-stu-id="6f011-132">After you've finished defining the "very late" transaction period, select **Create prediction model** to create the prediction model.</span></span> <span data-ttu-id="6f011-133">ส่วน **แบบจำลองการคาดคะเน** บนหน้า **พารามิเตอร์ข้อมูลเชิงลึกทางการเงิน** แสดงสถานะของแบบจำลองการคาดคะเน</span><span class="sxs-lookup"><span data-stu-id="6f011-133">The **Prediction model** section on the **Financial insights parameters** page shows the status of the prediction model.</span></span>

        > [!NOTE]
        > <span data-ttu-id="6f011-134">เมื่อใดก็ตามที่มีการสร้างแบบจำลองการคาดคะเน คุณสามารถเลือก **รีเซ็ตการสร้างแบบจำลอง** เพื่อเริ่มต้นกระบวนการได้</span><span class="sxs-lookup"><span data-stu-id="6f011-134">At any time while the prediction model is being created, you can select **Reset model creation** to restart the process.</span></span>

    <span data-ttu-id="6f011-135">ขณะนี้มีการตั้งค่าคอนฟิกลักษณะการทำงานแล้วและพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="6f011-135">The feature has now been configured and is ready to be used.</span></span>

<span data-ttu-id="6f011-136">หลังจากที่เปิดใช้งานลักษณะการทำงานแล้ว และตั้งค่าคอนฟิกแล้วและแบบจำลองการคาดคะเนถูกสร้างขึ้นแล้วและกำลังทำงานอยู่ ส่วน **แบบจำลองการคาดคะเน** ของหน้า **พารามิเตอร์ข้อมูลเชิงลึกทางการเงิน** แสดงความถูกต้องของแบบจำลองดังที่แสดงในภาพประกอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="6f011-136">After the feature has been turned on and configured, and the prediction model has been created and is working, the **Prediction model** section of the **Financial insights parameters** page shows the accuracy of the model, as shown in the following illustration.</span></span>

<span data-ttu-id="6f011-137">[![ความถูกต้องของแบบจำลองการคาดการณ์บนหน้าพารามิเตอร์ข้อมูลเชิงลึกทางการเงิน](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)</span><span class="sxs-lookup"><span data-stu-id="6f011-137">[![Accuracy of the prediction model on the Financial insights parameters page](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)</span></span>

## <a name="release-details"></a><span data-ttu-id="6f011-138">รายละเอียดการนำออกใช้</span><span class="sxs-lookup"><span data-stu-id="6f011-138">Release details</span></span>

<span data-ttu-id="6f011-139">ตัวอย่างข้อมูลเชิงลึกของการเงินสำหรับสาธารณะจะพร้อมใช้งานสำหรับการใช้งานทดลองในสหรัฐอเมริกา ยุโรป และสหราชอาณาจักร</span><span class="sxs-lookup"><span data-stu-id="6f011-139">Finance insights public preview is available for trial deployments in the United States of America, Europe, and the United Kingdom.</span></span> <span data-ttu-id="6f011-140">Microsoft กำลังเพิ่มการสนับสนุนสำหรับภูมิภาคเพิ่มเติมมากขึ้น</span><span class="sxs-lookup"><span data-stu-id="6f011-140">Microsoft is incrementally adding support for more regions.</span></span>

<span data-ttu-id="6f011-141">คุณลักษณะตัวอย่างสำหรับสาธารณะควรเปิดใช้งานเฉพาะในสภาพแวดล้อมที่มี Sandbox ระดับ 2 เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="6f011-141">Public preview features can and should be turned on only in Tier-2 sandbox environments.</span></span> <span data-ttu-id="6f011-142">การตั้งค่าและโมเดล AI ที่สร้างขึ้นในสภาพแวดล้อม Sandbox ไม่สามารถถูกย้ายไปยังสภาพแวดล้อมการผลิต</span><span class="sxs-lookup"><span data-stu-id="6f011-142">Setup and AI models that are created in a sandbox environment can't be migrated to a production environment.</span></span> <span data-ttu-id="6f011-143">สำหรับข้อมูลเพิ่มเติม ให้ดู [เงื่อนไขการใช้เพิ่มเติมสำหรับการแสดงตัวอย่าง Microsoft Dynamics 365](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms)</span><span class="sxs-lookup"><span data-stu-id="6f011-143">For more information, see [Supplemental Terms of Use for Microsoft Dynamics 365 Previews](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="6f011-144">ประกาศความเป็นส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="6f011-144">Privacy notice</span></span>

<span data-ttu-id="6f011-145">การแสดงตัวอย่าง (1) อาจใช้วิธีการที่มีความปลอดภัยและความเป็นส่วนตัวที่น้อยลงกว่าบริการ Dynamics 365 Finance and Operations (2) ไม่ถูกรวมอยู่ในข้อตกลงระดับการให้บริการ (SLA) สำหรับบริการนี้ (3) ไม่ควรถูกใช้เพื่อประมวลผลข้อมูลส่วนบุคคลหรือข้อมูลอื่นที่อยู่ภายใต้ข้อกำหนดการปฏิบัติตามกฎหมายหรือระเบียบข้อบังคับ และ (4) มีการสนับสนุนที่จำกัด</span><span class="sxs-lookup"><span data-stu-id="6f011-145">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
