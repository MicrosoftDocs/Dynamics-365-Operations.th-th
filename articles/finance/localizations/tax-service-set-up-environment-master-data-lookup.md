---
title: ตั้งค่าสภาพแวดล้อมการค้นหาข้อมูลหลัก
description: หัวข้อนี้อธิบายวิธีการตั้งค่าสภาพแวดล้อมของคุณเพื่อใช้ฟังก์ชันการค้นหาข้อมูลหลักของการคํานวณภาษี
author: kai-cloud
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: eda093a75898bace2f3c7968933b83ccafa7fabb
ms.sourcegitcommit: 66095f1b7e0fd2756aa29fd7deb9ce5392b7e0b2
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/08/2021
ms.locfileid: "5869103"
---
# <a name="set-up-an-environment-for-master-data-lookup"></a><span data-ttu-id="5acf4-103">ตั้งค่าสภาพแวดล้อมการค้นหาข้อมูลหลัก</span><span class="sxs-lookup"><span data-stu-id="5acf4-103">Set up an environment for master data lookup</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="5acf4-104">หัวข้อนี้อธิบายวิธีการตั้งค่าสภาพแวดล้อมของคุณเพื่อใช้ฟังก์ชันการค้นหาข้อมูลหลักของการคํานวณภาษี</span><span class="sxs-lookup"><span data-stu-id="5acf4-104">This topic explains how to set up your environment to use the Tax Calculation master data lookup functionality.</span></span>

1. <span data-ttu-id="5acf4-105">ตั้งค่าการรวม Power Platform ใน Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="5acf4-105">Set up power platform integration in Lifecycle Services (LCS).</span></span> <span data-ttu-id="5acf4-106">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [การรวม Microsoft Power Platform - ภาพรวม Add-in](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md)</span><span class="sxs-lookup"><span data-stu-id="5acf4-106">For more information, see [Microsoft Power Platform integration - Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).</span></span>
2. <span data-ttu-id="5acf4-107">ตั้งค่า Dynamics 365 Finance และ Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="5acf4-107">Set up Dynamics 365 Finance and Microsoft Dataverse.</span></span> <span data-ttu-id="5acf4-108">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [การรับโซลูชัน](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) และ [การรับรองความถูกต้องและการตรวจสอบความถูกต้อง](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization)</span><span class="sxs-lookup"><span data-stu-id="5acf4-108">For more information, see [Getting the solution](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) and [Authentication and authorization](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).</span></span>
3. <span data-ttu-id="5acf4-109">นําเข้า *โซลูชันเอนทิตีเสมือนของบริการภาษีตามข้อกำหนดเบื้องต้น* จาก [เอนทิตีเสมือนของบริการภาษี](https://go.microsoft.com/fwlink/?linkid=2158160)</span><span class="sxs-lookup"><span data-stu-id="5acf4-109">Import the *Prerequisite tax service virtual entity solution* from the [Tax service virtual entity](https://go.microsoft.com/fwlink/?linkid=2158160).</span></span>
4. <span data-ttu-id="5acf4-110">ตั้งค่า Dynamics 365 Regulatory Configuration Service (RCS)</span><span class="sxs-lookup"><span data-stu-id="5acf4-110">Set up the Dynamics 365 Regulatory Configuration Service (RCS).</span></span> 
5. <span data-ttu-id="5acf4-111">สร้างคำขอบริการเพื่อให้ Microsoft สามารถเปิดใช้งานเที่ยวบินของคุณลักษณะต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="5acf4-111">Create a service request for Microsoft to enable flighting of the following features:</span></span>

      - <span data-ttu-id="5acf4-112">ERCdsFeature</span><span class="sxs-lookup"><span data-stu-id="5acf4-112">ERCdsFeature</span></span>
      - <span data-ttu-id="5acf4-113">TaxServiceCDSFeature</span><span class="sxs-lookup"><span data-stu-id="5acf4-113">TaxServiceCDSFeature</span></span>

6. <span data-ttu-id="5acf4-114">ใน Finance ไปที่พื้นที่ทำงาน **การจัดการคุณลักษณะ** และเปิดใช้งานคุณลักษณะต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="5acf4-114">In Finance, go to the **Feature management** workspace, and enable the following features:</span></span>

      - <span data-ttu-id="5acf4-115">(การแสดงตัวอย่าง) การสนับสนุนแหล่งข้อมูล Dataverse การรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="5acf4-115">(Preview) Electronic reporting Dataverse datasources support</span></span>
      - <span data-ttu-id="5acf4-116">(พรีวิว) การสนับสนุนแหล่งข้อมูล Dataverse สำหรับบริการด้านภาษี</span><span class="sxs-lookup"><span data-stu-id="5acf4-116">(Preview) Tax Service Dataverse datasources support</span></span>
      - <span data-ttu-id="5acf4-117">(การแสดงตัวอย่าง) คุณลักษณะที่ใช้ทั่วโลก</span><span class="sxs-lookup"><span data-stu-id="5acf4-117">(Preview) Globalization features</span></span>

5. <span data-ttu-id="5acf4-118">เข้าสู่ระบบ RCS โดยใช้บัญชีผู้ดูแลระบบของผู้เช่า</span><span class="sxs-lookup"><span data-stu-id="5acf4-118">Sign in to RCS using a tenant admin account.</span></span>
6. <span data-ttu-id="5acf4-119">ไปที่ **การรายงานทางอิเล็กทรอนิกส์** > **โปรแกรมประยุกต์ที่เชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="5acf4-119">Go to **Electronic reporting** > **Connected applications**.</span></span> 
7. <span data-ttu-id="5acf4-120">เลือก **สร้าง** เพื่อเพิ่มเรกคอร์ด และป้อนข้อมูลฟิลด์ต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="5acf4-120">Select **New** to add a record, and enter the following field information.</span></span> 

   - <span data-ttu-id="5acf4-121">ในฟิลด์ **ชื่อ** ป้อนชื่อ</span><span class="sxs-lookup"><span data-stu-id="5acf4-121">In the **Name** field, enter a name.</span></span>
   - <span data-ttu-id="5acf4-122">ในฟิลด์ **ชนิด** เลือก **Dataverse**</span><span class="sxs-lookup"><span data-stu-id="5acf4-122">In the **Type** field, select **Dataverse**.</span></span>
   - <span data-ttu-id="5acf4-123">ในฟิลด์ **โปรแกรมประยุกต์** ให้ป้อน URL ของ Dataverse ของคุณ</span><span class="sxs-lookup"><span data-stu-id="5acf4-123">In the **Application** field, enter your Dataverse URL.</span></span>
   - <span data-ttu-id="5acf4-124">ในฟิลด์ **ผู้เช่า** ป้อนผู้เช่าของคุณ</span><span class="sxs-lookup"><span data-stu-id="5acf4-124">In the **Tenant** field, enter your tenant.</span></span>
   - <span data-ttu-id="5acf4-125">ในฟิลด์ **URL แบบกำหนดเอง** ให้ป้อน URL Dataverse ของคุณและผนวก URL ด้วย "/api/ข้อมูล/v9.1"</span><span class="sxs-lookup"><span data-stu-id="5acf4-125">In the **Custom URL** field, enter your Dataverse URL and append it with "/api/data/v9.1".</span></span>

8. <span data-ttu-id="5acf4-126">เลือก **ตรวจสอบการเชื่อมต่อ** และเสร็จสิ้นกระบวนการเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="5acf4-126">Select **Check connection**, and finish the connection process.</span></span> 

   <span data-ttu-id="5acf4-127">[![ตรวจสอบปุ่มการเชื่อมต่อ](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span><span class="sxs-lookup"><span data-stu-id="5acf4-127">[![Check connection button](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)</span></span>

9. <span data-ttu-id="5acf4-128">ไปที่ **การรายงานทางอิเล็กทรอนิกส์** > **การตั้งค่าคอนฟิกภาษี** และนําเข้าการตั้งค่าคอนฟิกภาษีจาก [การตั้งค่าคอนฟิกภาษี](https://go.microsoft.com/fwlink/?linkid=2158352)</span><span class="sxs-lookup"><span data-stu-id="5acf4-128">Go to **Electronic reporting** > **Tax configurations**, and import tax configurations from [Tax configurations](https://go.microsoft.com/fwlink/?linkid=2158352).</span></span>

   <span data-ttu-id="5acf4-129">[![หน้าการตั้งค่าคอนฟิกภาษี แผนภูมิรูปแบบข้อมูลภาษี](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span><span class="sxs-lookup"><span data-stu-id="5acf4-129">[![Tax configurations page, Tax data model tree](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)</span></span>

10. <span data-ttu-id="5acf4-130">ไปที่ **การแม็ปแบบจำลองเอกสารต้องเสียภาษี** หรือ **การแม็ปแบบจำลอง Dataverse** ถ้าคุณใช้การตั้งค่าคอนฟิก Microsoft และในฟิลด์ **โปรแกรมประยุกต์ที่เชื่อมต่อ** ให้เลือกเรกคอร์ดที่คุณสร้างไว้ในขั้นตอนที่ 7</span><span class="sxs-lookup"><span data-stu-id="5acf4-130">Go to the **Taxable document model mapping**, or **Dataverse Model Mapping** if you are using a Microsoft configuration, and in the **Connected application** field, select the record that you created in step 7.</span></span>
11. <span data-ttu-id="5acf4-131">ตั้งค่า **ค่าเริ่มต้นสำหรับการแม็ปแบบจำลอง** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="5acf4-131">Set **Default for model mapping** to **Yes**.</span></span>

   <span data-ttu-id="5acf4-132">[![หน้าการแม็ปแบบจำลอง](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span><span class="sxs-lookup"><span data-stu-id="5acf4-132">[![Model mapping page](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
