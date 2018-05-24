---
title: "การรวมกับ Microsoft Dynamics 365 for Field Service"
description: "หัวข้อนี้แสดงภาพรวมของการรวมกับ Microsoft Dynamics 365 for Field Service"
author: ChristianRytt
manager: AnnBe
ms.date: 04/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 03a932652cdd93b2a5917d0fca72809d1648b678
ms.openlocfilehash: b1acf0b64914a3199fcf44f8377e32b26f0af99e
ms.contentlocale: th-th
ms.lasthandoff: 04/25/2018

---


# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a><span data-ttu-id="c02f9-103">การรวมกับ Microsoft Dynamics 365 for Field Service</span><span class="sxs-lookup"><span data-stu-id="c02f9-103">Integration with Microsoft Dynamics 365 for Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c02f9-104">Microsoft Dynamics 365 for Finance and Operations เปิดใช้งานการซิงโครไนส์กระบวนการทางธุรกิจระหว่าง Finance and Operations และ Microsoft Dynamics 365 for Field Service</span><span class="sxs-lookup"><span data-stu-id="c02f9-104">Microsoft Dynamics 365 for Finance and Operations enables synchronization of business processes between Finance and Operations and Microsoft Dynamics 365 for Field Service.</span></span> <span data-ttu-id="c02f9-105">สถานการณ์จำลองการรวมถูกตั้งค่าคอนฟิกโดยใช้เท็มเพลตตัวรวมข้อมูลที่ขยายได้ และ Common Data Service (CDS) เพื่อเปิดใช้งานการซิงโครไนส์ของกระบวนการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="c02f9-105">The integration scenarios are configured by using extensible Data integrator templates and the Common Data Service (CDS) to enable the synchronization of business processes.</span></span>

<span data-ttu-id="c02f9-106">[![การซิงโครไนส์ของกระบวนการทางธุรกิจระหว่าง Finance and Operations และ Field Service](./media/field-service-integration.png)](./media/field-service-integration.png)</span><span class="sxs-lookup"><span data-stu-id="c02f9-106">[![Synchronization of business processes between Finance and Operations and Field Service](./media/field-service-integration.png)](./media/field-service-integration.png)</span></span>

<span data-ttu-id="c02f9-107">เฟสแรกของการรวมระหว่าง Field Service และ Finance and Operations จะเน้นบนการเปิดใช้งานใบสั่งผลิตและข้อตกลงใน Field Service ให้ออกใบแจ้งหนี้ใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c02f9-107">The first phase  of the integration between Field Service and Finance and Operations is focused on enabling work orders and agreements in Field Service to be invoiced in Finance and Operations.</span></span> <span data-ttu-id="c02f9-108">ขั้นตอนที่ได้รับการสนับสนุนเริ่มต้นใน Field Service ที่ซึ่งมีการซิงโครไนส์ข้อมูลจากใบสั่งผลิตไปยัง Finance and Operations เป็นใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="c02f9-108">The supported flow starts in Field Service, where information from work orders is synchronized to Finance and Operations as sales orders.</span></span> <span data-ttu-id="c02f9-109">ใน Finance and Operations ใบสั่งขายออกใบแจ้งหนี้เพื่อสร้างเอกสารใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="c02f9-109">In Finance and Operations, the sales orders are invoiced to generate invoice documents.</span></span> <span data-ttu-id="c02f9-110">นอกจากนี้ ข้อมูลจากใบแจ้งหนี้ของข้อตกลงของ Field Service จะซิงโครไนส์กับ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c02f9-110">In addition, the information from Field Service agreement invoices is synchronized to Finance and Operations.</span></span> <span data-ttu-id="c02f9-111">ตัวรวมข้อมูล Microsoft Dynamics 365 ซิงโครไนส์ข้อมูลโดยใช้โครงการที่กำหนดเองได้</span><span class="sxs-lookup"><span data-stu-id="c02f9-111">The Microsoft Dynamics 365 Data integrator synchronizes data by using customizable projects.</span></span> <span data-ttu-id="c02f9-112">เท็มเพลตมาตรฐานสามารถใช้เพื่อสร้างโครงการที่มีการรวมแบบกำหนดเอง ที่ซึ่งฟิลด์มาตรฐานและแบบกำหนดเองเพิ่มเติม และรวมทั้งเอนทิตี สามารถถูกแม็ปเพื่อปรับปรุงการรวม และให้ตรงตามข้อกำหนดเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="c02f9-112">Standard templates can be used to create custom integration projects where additional standard and custom fields, and also entities, can be mapped to adjust the integration and meet specific requirements.</span></span>

<span data-ttu-id="c02f9-113">เฟสแรกของการรวมระหว่าง Field Service และ Finance and Operations เปิดใช้งานการซิงโครไนส์ของรายการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c02f9-113">The first phase of the integration between Field Service and Finance and Operations enables synchronization of the following items:</span></span>

- [<span data-ttu-id="c02f9-114">ผลิตภัณฑ์ใน Finance and Operations ไปยังผลิตภัณฑ์ใน Field Service ที่รวมข้อมูลชนิดผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="c02f9-114">Products in Finance and Operations to products in Field Service that include Product Type information</span></span>](field-service-product.md)
- [<span data-ttu-id="c02f9-115">ใบสั่งผลิตใน Field Service ไปยังใบสั่งขายใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c02f9-115">Work orders in Field Service to sales orders in Finance and Operations</span></span>](field-service-work-order.md)
- [<span data-ttu-id="c02f9-116">ใบแจ้งหนี้ใน Field Service ไปยังใบแจ้งหนี้ข้อความอิสระใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c02f9-116">Invoices in Field Service to free text invoices in Finance and Operations</span></span>](field-service-invoice.md)

<span data-ttu-id="c02f9-117">เมื่อต้องการดูตัวอย่างของวิธีที่คุณสามารถซิงโครไนส์ใบสั่งงานระหว่าง Field Service และ Finance and Operations โปรดดูวิดีโอ YouTube แบบย่อ:</span><span class="sxs-lookup"><span data-stu-id="c02f9-117">To see an example of how you can synchronize a work order between Field Service and Finance and Operations, watch the short YouTube video:</span></span>

> [!Video https://www.youtube.com/embed/hAB4TDVMjxU]

[<span data-ttu-id="c02f9-118">ซิงโครไนส์ใบสั่งงานระหว่าง Field Service กับ Finance and Operations (วิดีโอ YouTube)</span><span class="sxs-lookup"><span data-stu-id="c02f9-118">Synchronize a work order between Field Service and Finance and Operations (YouTube video)</span></span>](https://youtu.be/hAB4TDVMjxU)

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="c02f9-119">ความต้องการของระบบสำหรับ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c02f9-119">System requirements for Finance and Operations</span></span>
<span data-ttu-id="c02f9-120">การรวม Field Service สนับสนุนเวอร์ชันต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c02f9-120">Field Service integration supports the following versions:</span></span>

### <a name="dynamics-365-for-finance-and-operations-version-80-april-2018-or-later"></a><span data-ttu-id="c02f9-121">Dynamics 365 for Finance and Operations รุ่น 8.0 (เมษายน 2018) หรือรุ่นที่ใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="c02f9-121">Dynamics 365 for Finance and Operations version 8.0 (April 2018) or later</span></span>

- <span data-ttu-id="c02f9-122">Dynamics 365 for Finance and Operations รุ่น 8.0 (เมษายน 2018) ถูกนำออกใช้ในเดือนเมษายน 2018 และได้สร้างแอพลิเคชันหมายเลข 8.0.30.8020 ที่มีการอัพเดแพลตฟอร์ม 15 (7.0.4841.35234)</span><span class="sxs-lookup"><span data-stu-id="c02f9-122">Dynamics 365 for Finance and Operations version 8.0 (April 2018) was released in April 2018 and has an application build number 8.0.30.8020 with Platform Update 15 (7.0.4841.35234).</span></span> 

## <a name="system-requirements-for-field-service"></a><span data-ttu-id="c02f9-123">ข้อกำหนดของระบบสำหรับ Field Service</span><span class="sxs-lookup"><span data-stu-id="c02f9-123">System requirements for Field Service</span></span>
<span data-ttu-id="c02f9-124">เมื่อต้องการใช้โซลูชันการรวม Field Service คุณต้องติดตั้งส่วนประกอบต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="c02f9-124">To use the Field Service integration solution, you must install the following components:</span></span>

### <a name="microsoft-dynamics-365-for-field-service-90-or-later"></a><span data-ttu-id="c02f9-125">Microsoft Dynamics 365 สำหรับ Field Service 9.0 หรือรุ่นที่ใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="c02f9-125">Microsoft Dynamics 365 for Field Service 9.0 or later</span></span>

- <span data-ttu-id="c02f9-126">Dynamics 365 for Field Service รุ่น 1612 (9.0.1.733) (DB 9.0.1.733) ออนไลน์ หรือรุ่นที่ใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="c02f9-126">Dynamics 365 for Field Service version 1612 (9.0.1.733) (DB 9.0.1.733) online or a later version.</span></span>
- <span data-ttu-id="c02f9-127">โซลูชันผู้ที่มีแนวโน้มจะเป็นลูกค้าเป็นเงินสด (P2C) สำหรับ Dynamics 365 รุ่น 1.15.0.1 หรือรุ่นที่ใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="c02f9-127">Prospect to Cash (P2C) solution for Dynamics 365, version 1.15.0.1 or a later version.</span></span> <span data-ttu-id="c02f9-128">โซลูชันนี้จะพร้อมใช้งานสำหรับการดาวน์โหลดจาก [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3)</span><span class="sxs-lookup"><span data-stu-id="c02f9-128">The solution is available for download from [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>
- <span data-ttu-id="c02f9-129">โซลูชันการรวม Field Service สำหรับ Dynamics 365 รุ่น 1.0.0.0 หรือรุ่นที่ใหม่กว่า</span><span class="sxs-lookup"><span data-stu-id="c02f9-129">Field Service integration solution for Dynamics 365, version 1.0.0.0 or a later version.</span></span> <span data-ttu-id="c02f9-130">โซลูชันนี้จะพร้อมใช้งานสำหรับการดาวน์โหลดจาก [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.p2cfieldserviceintegration)</span><span class="sxs-lookup"><span data-stu-id="c02f9-130">The solution is available for download from [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.p2cfieldserviceintegration).</span></span>

