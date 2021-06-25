---
title: เปิดใช้งานการคาดการณ์กระแสเงินสด (ตัวอย่าง)
description: หัวข้อนี้จะอธิบายวิธีการเปิดและตั้งค่าคอนฟิกลักษณะการทำงานการคาดการณ์กระแสเงินสดในข้อมูลเชิงลึกทางการเงิน
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: ba8acb2191291e2abed5cabf234c19fe09e6c8ff
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222569"
---
# <a name="enable-cash-flow-forecasting-preview"></a><span data-ttu-id="9e7d1-103">เปิดใช้งานการคาดการณ์กระแสเงินสด (ตัวอย่าง)</span><span class="sxs-lookup"><span data-stu-id="9e7d1-103">Enable cash flow forecasting (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="9e7d1-104">หัวข้อนี้จะอธิบายวิธีการเปิดและตั้งค่าคอนฟิกลักษณะการทำงานการคาดการณ์กระแสเงินสดในข้อมูลเชิงลึกทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="9e7d1-104">This topic explains how to turn on the Cash flow forecasts feature in Finance Insights.</span></span>

> [!NOTE]
> <span data-ttu-id="9e7d1-105">เมื่อต้องการใช้การคาดการณ์การชำระเงินในกระแสเงินสด คุณต้องตั้งค่าลักษณะการทำงานการคาดการณ์การชำระเงินของลูกค้าดังที่อธิบายไว้ใน [การเปิดใช้งานการคาดการณ์การชำระเงินของลูกค้า](enable-cust-paymnt-prediction.md)</span><span class="sxs-lookup"><span data-stu-id="9e7d1-105">To use payment predictions in the cash flow, you must set up the Customer payment predictions feature as described in [Enable customer payment predictions](enable-cust-paymnt-prediction.md).</span></span>

1. <span data-ttu-id="9e7d1-106">ใช้ข้อมูลจากหน้าสภาพแวดล้อมใน Microsoft Dynamics Lifecycle Services (LCS) เพื่อเชื่อมต่อกับอินสแตนซ์หลักของ AZURE SQL สำหรับสภาพแวดล้อมดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="9e7d1-106">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="9e7d1-107">รันคำสั่ง Transact-SQL (T-SQL) ต่อไปนี้เพื่อเปิดใช้งานเที่ยวบินสำหรับสภาพแวดล้อม sandbox</span><span class="sxs-lookup"><span data-stu-id="9e7d1-107">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="9e7d1-108">(คุณอาจต้องเปิดใช้งานการเข้าถึงสำหรับที่อยู่ IP ของคุณใน LCS ก่อนที่คุณจะสามารถเชื่อมต่อระยะไกลกับเซิร์ฟเวอออบเจ็กต์โปรแกรมประยุกต์ \[AOS\])</span><span class="sxs-lookup"><span data-stu-id="9e7d1-108">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('CashflowInsightsFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="9e7d1-109">ข้ามขั้นตอนนี้ถ้าคุณใช้รุ่น 10.0.20 หรือใหม่กว่า หรือถ้าคุณใช้งานการปรับใช้ Service Fabric</span><span class="sxs-lookup"><span data-stu-id="9e7d1-109">Skip this step if you're using version 10.0.20 or later, or if you're using a Service Fabric deployment.</span></span> <span data-ttu-id="9e7d1-110">ทีมงานในเชิงลึกของการเงินควรมีการเปิดใช้งานเที่ยวบินให้คุณแล้ว</span><span class="sxs-lookup"><span data-stu-id="9e7d1-110">The Finance insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="9e7d1-111">ถ้าคุณไม่เห็นคุณลักษณะในพื้นที่ทำงาน **การจัดการลักษณะการทำงาน** หรือหากประสบปัญหาเมื่อคุณพยายามเปิดใช้งาน โปรดติดต่อ <fiap@microsoft.com></span><span class="sxs-lookup"><span data-stu-id="9e7d1-111">If you don't see the feature in the **Feature management** workspace, or if you experience issues when you try to turn it on, contact <fiap@microsoft.com>.</span></span>
  
2. <span data-ttu-id="9e7d1-112">เปิดพื้นที่ทำงาน **การจัดการลักษณะการทำงาน** และปฏิบัติตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="9e7d1-112">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="9e7d1-113">เลือก **ตรวจหาการอัพเดต**</span><span class="sxs-lookup"><span data-stu-id="9e7d1-113">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="9e7d1-114">เปิดใช้งานคุณลักษณะต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="9e7d1-114">Turn on the following features:</span></span>

        - <span data-ttu-id="9e7d1-115">ตัวควบคุมเส้นตารางใหม่</span><span class="sxs-lookup"><span data-stu-id="9e7d1-115">New grid control</span></span>
        - <span data-ttu-id="9e7d1-116">การจัดกลุ่มในกริด (ตัวอย่าง)</span><span class="sxs-lookup"><span data-stu-id="9e7d1-116">Grouping in grids (preview)</span></span> 
        - <span data-ttu-id="9e7d1-117">การคาดคะเนการชำระเงินของลูกค้า (พรีวิว)</span><span class="sxs-lookup"><span data-stu-id="9e7d1-117">Customer payment predictions (preview)</span></span>
        - <span data-ttu-id="9e7d1-118">การคาดการณ์กระแสเงินสด (พรีวิว)</span><span class="sxs-lookup"><span data-stu-id="9e7d1-118">Cash flow forecasts (preview)</span></span>

3. <span data-ttu-id="9e7d1-119">ไปที่ **การจัดการธนาคารและเงินสด \> การตั้งค่าการคาดการณ์กระแสเงินสด** และเพิ่มบัญชีสภาพคล่องที่ควรรวมไว้ในการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="9e7d1-119">Go to **Cash and bank management \> Cash flow forecast setup**, and add the liquidity accounts that should be included in the forecasts.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9e7d1-120">ถ้าไม่ได้ตั้งค่าบัญชีสภาพคล่องไว้ แสดงว่าไม่สามารถสร้างกระแสเงินสดได้</span><span class="sxs-lookup"><span data-stu-id="9e7d1-120">If liquidity accounts aren't set up, the cash flow can't be generated.</span></span>

4. <span data-ttu-id="9e7d1-121">ไปที่ **การจัดการธนาคารและเงินสด \> การตั้งค่า \> ข้อมูลเชิงลึกทางการเงิน (ตัวอย่าง) \> การคาดการณ์กระแสเงินสด (ตัวอย่าง)** และปฏิบัติตามขั้นตอนเหล่านี้:</span><span class="sxs-lookup"><span data-stu-id="9e7d1-121">Go to **Cash and bank management \> Setup \> Finance Insights (preview) \> Cash flow forecasts (preview)**, and follow these steps:</span></span>

    1. <span data-ttu-id="9e7d1-122">บนแท็บ **การคาดการณ์กระแสเงินสด** เลือก **เปิดใช้งานลักษณะการทำงาน**</span><span class="sxs-lookup"><span data-stu-id="9e7d1-122">On the **Cash flow forecast** tab, select **Enable feature**.</span></span>
    2. <span data-ttu-id="9e7d1-123">เลือก **สร้างแบบจำลองการคาดการณ์**</span><span class="sxs-lookup"><span data-stu-id="9e7d1-123">Select **Create prediction model**.</span></span>

<span data-ttu-id="9e7d1-124">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับความสามารถการคาดการณ์กระแสเงินสด ให้ดู [การคาดการณ์กระแสเงินสด](cash-flow-forecast-intro.md)</span><span class="sxs-lookup"><span data-stu-id="9e7d1-124">For more information about the cash flow forecasting capability, see [Cash flow forecasting](cash-flow-forecast-intro.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
