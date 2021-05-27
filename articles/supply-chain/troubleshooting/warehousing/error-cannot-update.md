---
title: มีข้อผิดพลาดเกิดขึ้นเมื่อมีการเลือกสถานที่เก็บในระหว่างการลงทะเบียนรายการเบิกสินค้า
description: มีข้อผิดพลาดเกิดขึ้นเมื่อมีการเลือกสถานที่เก็บในระหว่างการลงทะเบียนรายการเบิกสินค้า
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: b7fc579821f9a80d94aea949fcc0301b9d8f6935
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026933"
---
# <a name="an-error-occurs-when-the-location-is-selected-during-picking-list-registration"></a><span data-ttu-id="fc72c-103">มีข้อผิดพลาดเกิดขึ้นเมื่อมีการเลือกสถานที่เก็บในระหว่างการลงทะเบียนรายการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="fc72c-103">An error occurs when the location is selected during picking list registration</span></span>

<span data-ttu-id="fc72c-104">หมายเลข KB: 4613106</span><span class="sxs-lookup"><span data-stu-id="fc72c-104">KB number: 4613106</span></span>

## <a name="symptoms"></a><span data-ttu-id="fc72c-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="fc72c-105">Symptoms</span></span>

<span data-ttu-id="fc72c-106">ปัญหานี้จะเกิดขึ้นเมื่อระบบของคุณมีการตั้งค่าคอนฟิกให้จองใบสั่งขายโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="fc72c-106">This issue occurs when your system is configured to automatically reserve sales orders.</span></span> <span data-ttu-id="fc72c-107">ถ้าคุณพยายามเลือกสถานที่เก็บสำหรับการลงทะเบียนรายการเบิกสินค้า คุณจะได้รับข้อความแสดงข้อผิดพลาดต่อไปนี้เมื่อคุณใช้กระบวนการจองการจัดการคลังสินค้า (WMS)</span><span class="sxs-lookup"><span data-stu-id="fc72c-107">If you try to select the location for a picking list registration line, you receive the following error message when you use warehouse management (WMS) reservation processes:</span></span>

> <span data-ttu-id="fc72c-108">ไม่สามารถอัปเดตปริมาณด้วยมิติใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="fc72c-108">Can't update quantity with new dimensions</span></span>

<span data-ttu-id="fc72c-109">ปัญหานี้อาจเกิดขึ้นได้ เนื่องจากคุณมีปริมาณคงคลังคงเหลือไม่เพียงพอที่สถานที่เก็บที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="fc72c-109">This issue can occur because you don't have enough on-hand inventory at a specified location.</span></span>

## <a name="resolution"></a><span data-ttu-id="fc72c-110">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="fc72c-110">Resolution</span></span>

<span data-ttu-id="fc72c-111">ระบบมีการทำงานตามที่ออกแบบ</span><span class="sxs-lookup"><span data-stu-id="fc72c-111">The system is behaving as designed.</span></span>

<span data-ttu-id="fc72c-112">ในสถานการณ์ที่คุณใช้กระบวนการจองระดับคลังสินค้า ถ้าปริมาณคงคลังคงเหลือจะไม่ถูกจองในระดับมิติสินค้าคงคลังทั้งหมด และคุณมีปริมาณคงคลังคงเหลือไม่เพียงพอ ณ สถานที่ที่ระบุ ขอแนะนำให้คุณใช้กระบวนการจองสินค้าด้วยตนเองจากรายการการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="fc72c-112">In scenarios where you use the warehouse-level reservation process, if the on-hand inventory won't be reserved on all inventory dimension levels, and you don't have enough on-hand inventory at a specified location, we recommend that you use the manual reservation process from the picking line.</span></span> <span data-ttu-id="fc72c-113">จากนั้นคุณสามารถใช้ฟังก์ชัน *จองล็อต* เพื่อกระจายการจองที่ต่ำกว่า เช่น สถานที่เก็บ ปริมาณคงคลังคงเหลือทั้งหมดที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="fc72c-113">You can then use the *Reserve lot* function to distribute the lower reservations, such as location, for all the available on-hand quantities.</span></span>
