---
title: ตัวเลือกการรายงานใน Talent
description: หัวข้อนี้อธิบายวิธีการแก้ปัญหาที่ซึ่งลูกค้าต้องการกำหนดค่ารายงาน Microsoft Dynamics 365 for Talent หรือสร้างรายงานใหม่
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 2007e6adec7255b0b3abda7490c2103a8583393f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "306478"
---
# <a name="reporting-options-in-talent"></a><span data-ttu-id="99ec5-103">ตัวเลือกการรายงานใน Talent</span><span class="sxs-lookup"><span data-stu-id="99ec5-103">Reporting options in Talent</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="99ec5-104">**รายละเอียดสภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="99ec5-104">**Environment details**</span></span>

<span data-ttu-id="99ec5-105">ปัญหานี้ใช้กับสภาพแวดล้อมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="99ec5-105">This issue applies to all environments.</span></span>

<span data-ttu-id="99ec5-106">**อาการ**</span><span class="sxs-lookup"><span data-stu-id="99ec5-106">**Symptom**</span></span>

<span data-ttu-id="99ec5-107">ลูกค้าต้องการกำหนดค่ารายงาน Microsoft Dynamics 365 for Talent หรือสร้างรายงานใหม่</span><span class="sxs-lookup"><span data-stu-id="99ec5-107">The customer wants to customize Microsoft Dynamics 365 for Talent reports or create new reports.</span></span>

<span data-ttu-id="99ec5-108">**ออกใช้**</span><span class="sxs-lookup"><span data-stu-id="99ec5-108">**Issue**</span></span>

<span data-ttu-id="99ec5-109">ผู้ใช้ไม่สามารถกำหนดค่ารายงาน Microsoft Power BI ที่ฝังอยู่ได้</span><span class="sxs-lookup"><span data-stu-id="99ec5-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="99ec5-110">**โซลูชัน**</span><span class="sxs-lookup"><span data-stu-id="99ec5-110">**Solution**</span></span>

- <span data-ttu-id="99ec5-111">ข้อมูล Core HR ที่ไหลไปยัง Common Data Service for Apps สามารถถูกรายงานได้ ผ่านตัวเชื่อมต่อ PowerApps CDS ไปยัง Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="99ec5-111">The Core HR data that flows to Common Data Service for Apps can be reported on via the PowerApps CDS connector to Power BI Desktop.</span></span> <span data-ttu-id="99ec5-112">โปรดทราบว่า Common Data Service for Apps ประกอบด้วยชุดย่อยของข้อมูล Core HR</span><span class="sxs-lookup"><span data-stu-id="99ec5-112">Note that Common Data Service for Apps contains a subset of Core HR data.</span></span> <span data-ttu-id="99ec5-113">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ Power BI และแดชบอร์ด ดู [สร้างรายงานและแดชบอร์ด Power BI ด้วย PowerApps Common Data Service](https://powerapps.microsoft.com/en-us/blog/cdsconnectortopowerbi)</span><span class="sxs-lookup"><span data-stu-id="99ec5-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with PowerApps Common Data Service](https://powerapps.microsoft.com/en-us/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="99ec5-114">การรายงานทางอิเล็กทรอนิกส์ (ER) พร้อมใช้งานสำหรับรายงานบางรายงานใน Talent</span><span class="sxs-lookup"><span data-stu-id="99ec5-114">Electronic reporting (ER) is available for some reports in Talent.</span></span> <span data-ttu-id="99ec5-115">สามารถทำการกำหนดค่าที่ควบคุมโดยลูกค้าได้โดยใช้ตัวเลือกการตั้งค่าคอนฟิก ER</span><span class="sxs-lookup"><span data-stu-id="99ec5-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="99ec5-116">ข้อมูลถูกส่งออกไปยัง Microsoft Excel หรือ Microsoft Word โดยใช้เอนทิตีข้อมูลต่างๆ ที่ Talent ให้ ผ่านทางการรวม Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="99ec5-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Talent provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="99ec5-117">**วิธีแก้ปัญหาระยะยาว**</span><span class="sxs-lookup"><span data-stu-id="99ec5-117">**Long-term solution**</span></span>

<span data-ttu-id="99ec5-118">ตัวเลือกการใช้ Power BI เพิ่มเติมจะพร้อมใช้งาน และข้อมูลและเอนทิตีเพิ่มเติมจะเป็นส่วนหนึ่งของ Common Data Service for Apps</span><span class="sxs-lookup"><span data-stu-id="99ec5-118">Additional Power BI options will be available, and more data and entities will be part of Common Data Service for Apps.</span></span>
