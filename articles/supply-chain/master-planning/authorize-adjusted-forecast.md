---
title: อนุมัติการคาดการณ์ที่ปรับปรุง
description: ไม่ใช่ข้อมูลการคาดการณ์ทั้งหมดจะต้องได้รับการอนุมัติในทันที บทความนี้อธิบายวิธีการที่คุณสามารถระบุรอบระยะเวลาที่การคาดการณ์ได้รับอนุมัติ ยังอธิบายถึงวิธีการอนุมัติการคาดการณ์สำหรับบริษัทที่ระบุและแบบจำลองการคาดการณ์อีกด้วย
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanImportForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72734
ms.assetid: cb8fd809-605a-4a8b-a390-636edfec21f9
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8ab8558f25f5ffd3b7eb3e1bc5680b1a1f8d5139
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4961474"
---
# <a name="authorize-an-adjusted-forecast"></a><span data-ttu-id="8558d-105">อนุมัติการคาดการณ์ที่ปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="8558d-105">Authorize an adjusted forecast</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8558d-106">ไม่ใช่ข้อมูลการคาดการณ์ทั้งหมดจะต้องได้รับการอนุมัติในทันที</span><span class="sxs-lookup"><span data-stu-id="8558d-106">Not all forecast data must be authorized immediately.</span></span> <span data-ttu-id="8558d-107">บทความนี้อธิบายวิธีการที่คุณสามารถระบุรอบระยะเวลาที่การคาดการณ์ได้รับอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="8558d-107">This article explains how you can specify the period that a forecast is authorized for.</span></span> <span data-ttu-id="8558d-108">ยังอธิบายถึงวิธีการอนุมัติการคาดการณ์สำหรับบริษัทที่ระบุและแบบจำลองการคาดการณ์อีกด้วย</span><span class="sxs-lookup"><span data-stu-id="8558d-108">It also explains how you can authorize the forecast for specific companies and forecast models.</span></span>

<span data-ttu-id="8558d-109">ไม่ใช่ข้อมูลการคาดการณ์ทั้งหมดจะต้องได้รับการอนุมัติในทันที</span><span class="sxs-lookup"><span data-stu-id="8558d-109">Not all forecast data must be authorized immediately.</span></span> <span data-ttu-id="8558d-110">คุณสามารถระบุวันที่เริ่มต้นและสิ้นสุดของรอบระยะเวลาที่การคาดการณ์ได้รับอนุญาต</span><span class="sxs-lookup"><span data-stu-id="8558d-110">You can specify the start and end dates of the period that the forecast is authorized for.</span></span> <span data-ttu-id="8558d-111">ฟังก์ชันนี้ช่วยให้คุณสามารถตรึงกลุ่มเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="8558d-111">This functionality lets you freeze specific buckets.</span></span> 

<span data-ttu-id="8558d-112">วันที่เริ่มต้นและสิ้นสุดที่คุณระบุจะต้องตรงกับวันที่เริ่มต้นและสิ้นสุดในกลุ่มที่มีสร้างการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="8558d-112">The start and end dates that you specify must correspond to the start and end dates of the bucket that the forecast is generated in.</span></span> <span data-ttu-id="8558d-113">ระบบจะบังคับใช้ข้อจำกัดนี้ และปรับปรุงวันที่โดยอัตโนมัติ ถ้าจำเป็นต้องมีการปรับปรุง</span><span class="sxs-lookup"><span data-stu-id="8558d-113">The system enforces this restriction and automatically adjusts the dates, if adjustment is required.</span></span> 

<span data-ttu-id="8558d-114">ในแท็บ **รายละเอียด** ของหน้า **การตรวจสอบ** คุณสามารถดูรายละเอียดเกี่ยวกับการคาดการณ์ที่ถูกสร้างขึ้นล่าสุดได้</span><span class="sxs-lookup"><span data-stu-id="8558d-114">On the **Details** tab of the **Authorization** page, you can view details about the forecast that was most recently generated.</span></span> 

<span data-ttu-id="8558d-115">คุณสามารถเลือกบริษัทและแบบจำลองการคาดการณ์เพื่ออนุมัติการคาดการณ์สำหรับการใช้ได้</span><span class="sxs-lookup"><span data-stu-id="8558d-115">You can select the companies and the forecast models to authorize the forecast for use.</span></span> <span data-ttu-id="8558d-116">โดยค่าเริ่มต้น กริดประกอบด้วยบริษัททั้งหมดที่มีการสร้างการคาดการณ์ความต้องการให้</span><span class="sxs-lookup"><span data-stu-id="8558d-116">By default, the grid includes all the companies that forecast demand has been created for.</span></span> <span data-ttu-id="8558d-117">สำหรับบริษัทแต่ละบริษัท แบบจำลองการคาดการณ์ที่เกี่ยวข้องกับแผนการคาดการณ์ปัจจุบันที่ถูกตั้งค่าในพารามิเตอร์การวางแผนหลักจะมีการกรอกข้อมูลล่วงหน้าไว้</span><span class="sxs-lookup"><span data-stu-id="8558d-117">For each company, the forecast model that corresponds to the current forecast plan that is set up in the master planning parameters is prefilled.</span></span> <span data-ttu-id="8558d-118">อย่างไรก็ตาม คุณสามารถเปลี่ยนแบบจำลองการคาดการณ์นี้ไปเป็นแบบจำลองการคาดการณ์ใดๆที่เป็นของบริษัทนั้น</span><span class="sxs-lookup"><span data-stu-id="8558d-118">However, you can change this forecast model to any forecast model that belongs to that company.</span></span> <span data-ttu-id="8558d-119">ถ้าไม่มีการสร้างงข้อมูลความต้องการการคาดการณ์สำหรับบริษัทที่เลือก คุณจะได้รับข้อความเตือนในขณะนำเข้า</span><span class="sxs-lookup"><span data-stu-id="8558d-119">If no forecast demand data has been generated for a selected company, you receive a warning message at import time.</span></span> 

<span data-ttu-id="8558d-120">สำคัญอย่างยิ่งว่าคุณเข้าใจวิธีการทำงานของกล่องกาเครื่องหมาย **บันทึกการปรับปรุงด้วยตนเองที่ทำต่อการคาดการณ์ความต้องการพื้นฐาน**</span><span class="sxs-lookup"><span data-stu-id="8558d-120">It's very important that you understand how the **Save the manual adjustments made to the baseline demand forecast** check box works.</span></span> <span data-ttu-id="8558d-121">ถ้าคุณได้ทำการปรับปรุงด้วยตนเองไปยังการคาดการณ์พื้นฐานทางสถิติ ค่าที่มีการปรับปรุงจะได้รับอนุญาตให้ใช้ ถึงแม้ว่าจะมีการล้างกล่องกาเครื่องหมายนี้</span><span class="sxs-lookup"><span data-stu-id="8558d-121">If you've made manual adjustments to the statistical baseline forecast, the adjusted values are authorized for use, even if this check box is cleared.</span></span> <span data-ttu-id="8558d-122">อย่างไรก็ตาม การเปลี่ยนแปลงจะถูกละทิ้งหลังจากการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="8558d-122">However, the changes are discarded after the authorization.</span></span> <span data-ttu-id="8558d-123">ดังนั้น ครั้งถัดไปที่มีสร้างการคาดการณ์ การคาดการณ์จะเป็นการคาดการณ์ทางสถิติเท่านั้น และไม่มีการแทนที่ด้วยตนเองใดๆ ถึงแม้ว่าจะมีการเลือก **การปรับปรุงการโอนย้ายด้วยตนเองไปยังการคาดการณ์ความต้องการ**</span><span class="sxs-lookup"><span data-stu-id="8558d-123">Therefore, the next time that a forecast is generated, that forecast is only a statistical forecast and doesn't have any manual overrides, even if **Transfer manual adjustments to the demand forecast** is selected.</span></span> <span data-ttu-id="8558d-124">ดังนั้น คุณสามารถพิจารณากล่องกาเครื่องหมาย **บันทึกการปรับปรุงด้วยตนเองที่ทำต่อการคาดการณ์ความต้องการพื้นฐาน** เป็นกลไกที่ช่วยให้คุณสามารถเก็บ หรือละทิ้งการเปลี่ยนแปลงทั้งหมดที่ดำเนินการด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="8558d-124">Therefore, you can consider the **Save the manual adjustments made to the baseline demand forecast** check box a mechanism that lets you keep or discard all manual changes.</span></span>

<a name="additional-resources"></a><span data-ttu-id="8558d-125">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="8558d-125">Additional resources</span></span>
--------

[<span data-ttu-id="8558d-126">ทำการปรับปรุงด้วยตนเองไปยังการคาดการณ์พื้นฐาน</span><span class="sxs-lookup"><span data-stu-id="8558d-126">Make manual adjustments to the baseline forecast</span></span>](manual-adjustments-baseline-forecast.md)

[<span data-ttu-id="8558d-127">ตรวจสอบความถูกต้องของการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="8558d-127">Monitor forecast accuracy</span></span>](monitor-forecast-accuracy.md)



