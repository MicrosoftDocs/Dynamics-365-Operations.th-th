---
title: รายงานเมื่อเสร็จไปยังสถานที่ที่ควบคุมป้ายทะเบียนจากอุปกรณ์สำหรับบัตรงาน
description: หัวข้อนี้อธิบายกระบวนการสำหรับการดำเนินการผลิตภัณฑ์สำเร็จรูปในใบสั่งผลิตไปยังสินค้าคงคลังเมื่อป้ายทะเบียนควบคุมที่ตั้ง
author: johanhoffmann
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistration, ProdJournalTransJob, ProdJournalTransRoute, ProdParmReportFinished
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19351
ms.assetid: bcc9e242-b4b8-4144-b14d-c3c106fb40ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2019-09-06
ms.dyn365.ops.version: AX 10.0.6
ms.openlocfilehash: 35ad27a6b8a52bfd086fbe4fc57b1681ff88fd5b
ms.sourcegitcommit: 58db26b7edf02e7c33aaaf1c934e3263aa74b01f
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/11/2019
ms.locfileid: "1995153"
---
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a><span data-ttu-id="b321f-103">รายงานเมื่อเสร็จไปยังสถานที่ที่ควบคุมป้ายทะเบียนจากอุปกรณ์สำหรับบัตรงาน</span><span class="sxs-lookup"><span data-stu-id="b321f-103">Report as finished to a license plate controlled location from the Job card device</span></span> 

<span data-ttu-id="b321f-104">กระบวนการที่เรียกว่ารายงานเมื่อผลิตภัณฑ์สำเร็จรูปในใบสั่งผลิตเสร็จสมบูรณ์จนส่งไปยังสินค้าคงคลัง</span><span class="sxs-lookup"><span data-stu-id="b321f-104">The process called Reporting as finished completes finished products on a production order to the inventory.</span></span> <span data-ttu-id="b321f-105">ถ้าผลิตภัณฑ์สำเร็จรูปถูกเปิดใช้งานสำหรับกระบวนการคลังสินค้าขั้นสูง ผลิตภัณฑ์จะถูกรายงานว่าสำเร็จไปยังสถานที่ที่เรียกว่าที่สถานที่ผลิตผลผลิต</span><span class="sxs-lookup"><span data-stu-id="b321f-105">If the finished product is enabled for the advanced warehouse processes, the product is reported as finished to a location called the production output location.</span></span> <span data-ttu-id="b321f-106">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการตั้งค่าสถานที่ผลิตผลผลิต กรุณาดูที่ [สถานที่ผลิตผลผลิต](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location)</span><span class="sxs-lookup"><span data-stu-id="b321f-106">For information about setting up the production output location, see [Production output location](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).</span></span>

<span data-ttu-id="b321f-107">คุณต้องเลือกหมายเลขป้ายทะเบียนที่มีอยู่เพื่อทำให้งานนี้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="b321f-107">You must select an existing license plate number to complete this task.</span></span> <span data-ttu-id="b321f-108">ถ้าสถานที่ผลิตผลผลิตมีการตั้งค่าที่ตั้งไว้เพื่อติดตามโดยป้ายทะเบียน สถานที่ผลิตผลผลิตจะต้องระบุหมายเลขป้ายทะเบียนเมื่อรายงานสถานที่ผลิตผลผลิตเมื่อผลิตเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="b321f-108">If the production output location is set up to be tracked by license plate, then a license plate number must be included when reporting the production output location as finished.</span></span> <span data-ttu-id="b321f-109">ฟิลด์ **ป้ายทะเบียน** จะปรากฏทันทีบน **รายงานความคืบหน้า** บนหน้า **อุปกรณ์สำหรับบัตรงาน**</span><span class="sxs-lookup"><span data-stu-id="b321f-109">The **License plate** field is visible on the **Report progress** prompt on the **Job card device** page.</span></span> <span data-ttu-id="b321f-110">ฟิลด์นี้จะปรากฏทันที **รายงานความคืบหน้า** เมื่อรายงานเกี่ยวกับการดำเนินงานครั้งสุดท้ายของใบสั่งผลิต</span><span class="sxs-lookup"><span data-stu-id="b321f-110">The field is only visible on the **Report progress** prompt when reporting on the last operation of the production order.</span></span> <span data-ttu-id="b321f-111">ฟิลด์นี้จะแสดงเฉพาะเมื่อสินค้าสำหรับใบสั่งผลิตถูกเปิดใช้งานสำหรับกระบวนการจัดการคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="b321f-111">The field is only shown if the item for the production order is enabled for the warehouse management processes.</span></span> 
