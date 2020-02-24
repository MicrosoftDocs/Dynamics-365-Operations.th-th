---
title: ตัวเลือกในการรายงาน
description: บทความนี้อธิบายวิธีการแก้ปัญหาที่ซึ่งลูกค้าต้องการกำหนดค่ารายงาน Microsoft Dynamics 365 Human Resources หรือสร้างรายงานใหม่
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9ee6dba5e37877f1c0b3b9df8306b3194ea2f3e4
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010803"
---
# <a name="reporting-options"></a><span data-ttu-id="2f170-103">ตัวเลือกในการรายงาน</span><span class="sxs-lookup"><span data-stu-id="2f170-103">Reporting options</span></span>

<span data-ttu-id="2f170-104">**รายละเอียดสภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="2f170-104">**Environment details**</span></span>

<span data-ttu-id="2f170-105">ปัญหานี้ใช้กับสภาพแวดล้อมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="2f170-105">This issue applies to all environments.</span></span>

<span data-ttu-id="2f170-106">**อาการ**</span><span class="sxs-lookup"><span data-stu-id="2f170-106">**Symptom**</span></span>

<span data-ttu-id="2f170-107">ลูกค้าต้องการกำหนดค่ารายงาน Microsoft Dynamics 365 Human Resources หรือสร้างรายงานใหม่</span><span class="sxs-lookup"><span data-stu-id="2f170-107">The customer wants to customize Microsoft Dynamics 365 Human Resources reports or create new reports.</span></span>

<span data-ttu-id="2f170-108">**ออกใช้**</span><span class="sxs-lookup"><span data-stu-id="2f170-108">**Issue**</span></span>

<span data-ttu-id="2f170-109">ผู้ใช้ไม่สามารถกำหนดค่ารายงาน Microsoft Power BI ที่ฝังอยู่ได้</span><span class="sxs-lookup"><span data-stu-id="2f170-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="2f170-110">**โซลูชัน**</span><span class="sxs-lookup"><span data-stu-id="2f170-110">**Solution**</span></span>

- <span data-ttu-id="2f170-111">ข้อมูลทรัพยากรบุคคลที่ไหลไปยัง Common Data Service สามารถถูกรายงานได้ผ่านตัวเชื่อมต่อ Power Apps Common Data Service ไปยัง Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="2f170-111">The Human Resources data that flows to Common Data Service can be reported on via the Power Apps Common Data Service connector to Power BI Desktop.</span></span> <span data-ttu-id="2f170-112">โปรดทราบว่า Common Data Service ประกอบด้วยชุดย่อยของข้อมูลทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="2f170-112">Note that Common Data Service contains a subset of Human Resources data.</span></span> <span data-ttu-id="2f170-113">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ Power BI และแดชบอร์ด ดู [สร้างรายงานและแดชบอร์ด Power BI ด้วย Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi)</span><span class="sxs-lookup"><span data-stu-id="2f170-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="2f170-114">การรายงานทางอิเล็กทรอนิกส์ (ER) พร้อมใช้งานสำหรับรายงานบางรายงานในทรัพยากรบุคคล</span><span class="sxs-lookup"><span data-stu-id="2f170-114">Electronic reporting (ER) is available for some reports in Human Resources.</span></span> <span data-ttu-id="2f170-115">สามารถทำการกำหนดค่าที่ควบคุมโดยลูกค้าได้โดยใช้ตัวเลือกการตั้งค่าคอนฟิก ER</span><span class="sxs-lookup"><span data-stu-id="2f170-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="2f170-116">ข้อมูลถูกส่งออกไปยัง Microsoft Excel หรือ Microsoft Word โดยใช้เอนทิตีข้อมูลต่าง ๆ ที่ทรัพยากรบุคคลให้ ผ่านทางการรวม Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="2f170-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Human Resources provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="2f170-117">**วิธีแก้ปัญหาระยะยาว**</span><span class="sxs-lookup"><span data-stu-id="2f170-117">**Long-term solution**</span></span>

<span data-ttu-id="2f170-118">ตัวเลือก Power BI เพิ่มเติมจะพร้อมใช้งาน และข้อมูลและเอนทิตีเพิ่มเติมจะเป็นส่วนหนึ่งของ Common Data Service</span><span class="sxs-lookup"><span data-stu-id="2f170-118">Additional Power BI options will be available, and more data and entities will be part of Common Data Service.</span></span>
