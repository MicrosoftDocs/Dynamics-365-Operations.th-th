---
title: เปิดใช้งานการคาดการณ์กระแสเงินสด (ตัวอย่าง)
description: หัวข้อนี้จะอธิบายวิธีการเปิดและตั้งค่าคอนฟิกลักษณะการทำงานการคาดการณ์กระแสเงินสดในข้อมูลเชิงลึกทางการเงิน
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/24/2020
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
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 321c716c10b136769ea3a48a3b60a8a717798338
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646240"
---
# <a name="enable-cash-flow-forecasting-preview"></a><span data-ttu-id="06b06-103">เปิดใช้งานการคาดการณ์กระแสเงินสด (ตัวอย่าง)</span><span class="sxs-lookup"><span data-stu-id="06b06-103">Enable cash flow forecasting (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="06b06-104">หัวข้อนี้จะอธิบายวิธีการเปิดและตั้งค่าคอนฟิกลักษณะการทำงานการคาดการณ์กระแสเงินสดในข้อมูลเชิงลึกทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="06b06-104">This topic explains how to turn on the Cash flow forecasts feature in Finance Insights.</span></span>

> [!NOTE]
> <span data-ttu-id="06b06-105">เมื่อต้องการใช้การคาดการณ์การชำระเงินในกระแสเงินสด คุณต้องตั้งค่าลักษณะการทำงานการคาดการณ์การชำระเงินของลูกค้าดังที่อธิบายไว้ใน [การเปิดใช้งานการคาดการณ์การชำระเงินของลูกค้า](enable-cust-paymnt-prediction.md)</span><span class="sxs-lookup"><span data-stu-id="06b06-105">To use payment predictions in the cash flow, you must set up the Customer payment predictions feature as described in [Enable customer payment predictions](enable-cust-paymnt-prediction.md).</span></span>

1. <span data-ttu-id="06b06-106">ใช้ข้อมูลจากหน้าสภาพแวดล้อมใน Microsoft Dynamics Lifecycle Services (LCS) เพื่อเชื่อมต่อกับอินสแตนซ์หลักของ AZURE SQL สำหรับสภาพแวดล้อมดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="06b06-106">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="06b06-107">รันคำสั่ง Transact-SQL (T-SQL) ต่อไปนี้เพื่อเปิดใช้งานเที่ยวบินสำหรับสภาพแวดล้อม sandbox</span><span class="sxs-lookup"><span data-stu-id="06b06-107">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="06b06-108">(คุณอาจต้องเปิดใช้งานการเข้าถึงสำหรับที่อยู่ IP ของคุณใน LCS ก่อนที่คุณจะสามารถเชื่อมต่อระยะไกลกับเซิร์ฟเวอออบเจ็กต์โปรแกรมประยุกต์ \[AOS\])</span><span class="sxs-lookup"><span data-stu-id="06b06-108">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('CashflowInsightsFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="06b06-109">ถ้าการปรับใช้ Microsoft Dynamics 365 Finance ของคุณเป็นการปรับใช้การให้บริการ คุณสามารถข้ามขั้นตอนนี้ได้</span><span class="sxs-lookup"><span data-stu-id="06b06-109">If your deployment of Microsoft Dynamics 365 Finance is a Service Fabric deployment, you can skip this step.</span></span> <span data-ttu-id="06b06-110">ทีมงานในเชิงลึกของการเงินควรมีการเปิดใช้งานเที่ยวบินให้คุณแล้ว</span><span class="sxs-lookup"><span data-stu-id="06b06-110">The Finance Insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="06b06-111">ถ้าคุณไม่เห็นคุณลักษณะในพื้นที่ทำงาน **การจัดการลักษณะการทำงาน** หรือหากประสบปัญหาเมื่อคุณพยายามเปิดใช้งาน โปรดติดต่อ <fiap@microsoft.com></span><span class="sxs-lookup"><span data-stu-id="06b06-111">If you don't see the features in the **Feature management** workspace, or if experience issues when you try to turn them on, contact <fiap@microsoft.com>.</span></span>
  
2. <span data-ttu-id="06b06-112">เปิดพื้นที่ทำงาน **การจัดการลักษณะการทำงาน** และปฏิบัติตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="06b06-112">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="06b06-113">เลือก **ตรวจหาการอัพเดต**</span><span class="sxs-lookup"><span data-stu-id="06b06-113">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="06b06-114">เปิดใช้งานคุณลักษณะต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="06b06-114">Turn on the following features:</span></span>

        - <span data-ttu-id="06b06-115">ตัวควบคุมเส้นตารางใหม่</span><span class="sxs-lookup"><span data-stu-id="06b06-115">New grid control</span></span>
        - <span data-ttu-id="06b06-116">การจัดกลุ่มในกริด (ตัวอย่าง)</span><span class="sxs-lookup"><span data-stu-id="06b06-116">Grouping in grids (preview)</span></span> 
        - <span data-ttu-id="06b06-117">การคาดคะเนการชำระเงินของลูกค้า (พรีวิว)</span><span class="sxs-lookup"><span data-stu-id="06b06-117">Customer payment predictions (preview)</span></span>
        - <span data-ttu-id="06b06-118">การคาดการณ์กระแสเงินสด (พรีวิว)</span><span class="sxs-lookup"><span data-stu-id="06b06-118">Cash flow forecasts (preview)</span></span>

3. <span data-ttu-id="06b06-119">ไปที่ **การจัดการธนาคารและเงินสด \> การตั้งค่าการคาดการณ์กระแสเงินสด** และเพิ่มบัญชีสภาพคล่องที่ควรรวมไว้ในการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="06b06-119">Go to **Cash and bank management \> Cash flow forecast setup**, and add the liquidity accounts that should be included in the forecasts.</span></span>

    > [!NOTE]
    > <span data-ttu-id="06b06-120">ถ้าไม่ได้ตั้งค่าบัญชีสภาพคล่องไว้ แสดงว่าไม่สามารถสร้างกระแสเงินสดได้</span><span class="sxs-lookup"><span data-stu-id="06b06-120">If liquidity accounts aren't set up, the cash flow can't be generated.</span></span>

4. <span data-ttu-id="06b06-121">ไปที่ **การจัดการธนาคารและเงินสด \> การตั้งค่า \> ข้อมูลเชิงลึกทางการเงิน (ตัวอย่าง) \> การคาดการณ์กระแสเงินสด (ตัวอย่าง)** และปฏิบัติตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="06b06-121">Go to **Cash and bank management \> Setup \> Finance Insights (preview) \> Cash flow forecasts (preview)**, and follow these steps:</span></span>

    1. <span data-ttu-id="06b06-122">บนแท็บ **การคาดการณ์กระแสเงินสด** เลือก **เปิดใช้งานลักษณะการทำงาน**</span><span class="sxs-lookup"><span data-stu-id="06b06-122">On the **Cash flow forecast** tab, select **Enable feature**.</span></span>
    2. <span data-ttu-id="06b06-123">เลือก **สร้างแบบจำลองการคาดการณ์**</span><span class="sxs-lookup"><span data-stu-id="06b06-123">Select **Create prediction model**.</span></span>

<span data-ttu-id="06b06-124">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับความสามารถการคาดการณ์กระแสเงินสด ให้ดู [การคาดการณ์กระแสเงินสด](cash-flow-forecast-intro.md)</span><span class="sxs-lookup"><span data-stu-id="06b06-124">For more information about the cash flow forecasting capability, see [Cash flow forecasting](cash-flow-forecast-intro.md).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="06b06-125">ประกาศความเป็นส่วนตัว</span><span class="sxs-lookup"><span data-stu-id="06b06-125">Privacy notice</span></span>

<span data-ttu-id="06b06-126">การแสดงตัวอย่าง (1) อาจใช้วิธีการที่มีความปลอดภัยและความเป็นส่วนตัวที่น้อยลงกว่าบริการ Dynamics 365 Finance and Operations (2) ไม่ถูกรวมอยู่ในข้อตกลงระดับการให้บริการ (SLA) สำหรับบริการนี้ (3) ไม่ควรถูกใช้เพื่อประมวลผลข้อมูลส่วนบุคคลหรือข้อมูลอื่นที่อยู่ภายใต้ข้อกำหนดการปฏิบัติตามกฎหมายหรือระเบียบข้อบังคับ และ (4) มีการสนับสนุนที่จำกัด</span><span class="sxs-lookup"><span data-stu-id="06b06-126">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
