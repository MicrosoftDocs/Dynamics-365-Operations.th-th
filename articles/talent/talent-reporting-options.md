---
title: ตัวเลือกการรายงานใน Talent
description: หัวข้อนี้อธิบายวิธีการแก้ปัญหาที่ซึ่งลูกค้าต้องการกำหนดค่ารายงาน Microsoft Dynamics 365 Talent หรือสร้างรายงานใหม่
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 05d4a2c4314b40042ae45b4f653554bad09be4fa
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897959"
---
# <a name="reporting-options-in-talent"></a><span data-ttu-id="eb540-103">ตัวเลือกการรายงานใน Talent</span><span class="sxs-lookup"><span data-stu-id="eb540-103">Reporting options in Talent</span></span>

<span data-ttu-id="eb540-104">**รายละเอียดสภาพแวดล้อม**</span><span class="sxs-lookup"><span data-stu-id="eb540-104">**Environment details**</span></span>

<span data-ttu-id="eb540-105">ปัญหานี้ใช้กับสภาพแวดล้อมทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="eb540-105">This issue applies to all environments.</span></span>

<span data-ttu-id="eb540-106">**อาการ**</span><span class="sxs-lookup"><span data-stu-id="eb540-106">**Symptom**</span></span>

<span data-ttu-id="eb540-107">ลูกค้าต้องการกำหนดค่ารายงาน Microsoft Dynamics 365 Talent หรือสร้างรายงานใหม่</span><span class="sxs-lookup"><span data-stu-id="eb540-107">The customer wants to customize Microsoft Dynamics 365 Talent reports or create new reports.</span></span>

<span data-ttu-id="eb540-108">**ออกใช้**</span><span class="sxs-lookup"><span data-stu-id="eb540-108">**Issue**</span></span>

<span data-ttu-id="eb540-109">ผู้ใช้ไม่สามารถกำหนดค่ารายงาน Microsoft Power BI ที่ฝังอยู่ได้</span><span class="sxs-lookup"><span data-stu-id="eb540-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="eb540-110">**โซลูชัน**</span><span class="sxs-lookup"><span data-stu-id="eb540-110">**Solution**</span></span>

- <span data-ttu-id="eb540-111">ข้อมูล Core HR ที่ไหลไปยัง Common Data Service สามารถถูกรายงานได้ผ่านตัวเชื่อมต่อ Power Apps Common Data Service ไปยัง Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="eb540-111">The Core HR data that flows to Common Data Service can be reported on via the Power Apps Common Data Service connector to Power BI Desktop.</span></span> <span data-ttu-id="eb540-112">โปรดทราบว่า Common Data Service ประกอบด้วยชุดย่อยของข้อมูล Core HR</span><span class="sxs-lookup"><span data-stu-id="eb540-112">Note that Common Data Service contains a subset of Core HR data.</span></span> <span data-ttu-id="eb540-113">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับ Power BI และแดชบอร์ด ดู [สร้างรายงานและแดชบอร์ด Power BI ด้วย Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi)</span><span class="sxs-lookup"><span data-stu-id="eb540-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="eb540-114">การรายงานทางอิเล็กทรอนิกส์ (ER) พร้อมใช้งานสำหรับรายงานบางรายงานใน Talent</span><span class="sxs-lookup"><span data-stu-id="eb540-114">Electronic reporting (ER) is available for some reports in Talent.</span></span> <span data-ttu-id="eb540-115">สามารถทำการกำหนดค่าที่ควบคุมโดยลูกค้าได้โดยใช้ตัวเลือกการตั้งค่าคอนฟิก ER</span><span class="sxs-lookup"><span data-stu-id="eb540-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="eb540-116">ข้อมูลถูกส่งออกไปยัง Microsoft Excel หรือ Microsoft Word โดยใช้เอนทิตีข้อมูลต่างๆ ที่ Talent ให้ ผ่านทางการรวม Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="eb540-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Talent provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="eb540-117">**วิธีแก้ปัญหาระยะยาว**</span><span class="sxs-lookup"><span data-stu-id="eb540-117">**Long-term solution**</span></span>

<span data-ttu-id="eb540-118">ตัวเลือก Power BI เพิ่มเติมจะพร้อมใช้งาน และข้อมูลและเอนทิตีเพิ่มเติมจะเป็นส่วนหนึ่งของ Common Data Service</span><span class="sxs-lookup"><span data-stu-id="eb540-118">Additional Power BI options will be available, and more data and entities will be part of Common Data Service.</span></span>
