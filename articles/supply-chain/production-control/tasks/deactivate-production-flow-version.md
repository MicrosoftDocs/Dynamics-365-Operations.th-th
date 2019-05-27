---
title: ยกเลิกการเรียกใช้เวอร์ชันขั้นตอนการผลิต
description: 'เมื่อไม่ต้องการรุ่นของขั้นตอนการผลิตที่ใช้งานอยู่แล้ว สามารถถูกปิดใช้งานได้ '
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 091cafd02bd568323e586373fc8b0f983afee343
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565265"
---
# <a name="deactivate-a-production-flow-version"></a><span data-ttu-id="3ee79-103">ยกเลิกการเรียกใช้เวอร์ชันขั้นตอนการผลิต</span><span class="sxs-lookup"><span data-stu-id="3ee79-103">Deactivate a production flow version</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3ee79-104">เมื่อไม่ต้องการรุ่นของขั้นตอนการผลิตที่ใช้งานอยู่แล้ว สามารถถูกปิดใช้งานได้ </span><span class="sxs-lookup"><span data-stu-id="3ee79-104">When an active production flow version is no longer needed, it can be deactivated.</span></span> <span data-ttu-id="3ee79-105">คุณควรใช้ตัวเลือกนี้หากกฎคัมบังและกิจกรรมทั้งหมดสิ้นแล้ว และจะไม่ทำงานอีกครั้งเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="3ee79-105">You should only use this option if all kanban rules and activities have ended and will not be activated again.</span></span> <span data-ttu-id="3ee79-106">โปรดทราบว่า วันที่หมดอายุของกฎคัมบังทั้งหมดที่เกี่ยวข้องกับเวอร์ชันขั้นตอนการผลิตนี้จะถูกปรับปรุงด้วยวันที่ปัจจุบันและเวลา</span><span class="sxs-lookup"><span data-stu-id="3ee79-106">Note that the expiry date of all kanban rules related to this production flow version will be updated with the current date and time.</span></span> 

<span data-ttu-id="3ee79-107">เมื่อต้องการแก้ไขเวอร์ชันขั้นตอนการผลิตที่ใช้งานอยู่ พิจารณาการตั้งค่าวันหมดอายุสำหรับเวอร์ชันที่ใช้งานอยู่ และสร้างเวอร์ชันใหม่</span><span class="sxs-lookup"><span data-stu-id="3ee79-107">To modify an active production flow version, consider setting an expiry date for the active version and create a new version.</span></span> <span data-ttu-id="3ee79-108">ซึ่งจะอนุญาตให้คุณดำเนินต่อการดำเนินงานผลิตต่อขณะกำลังเตรียมเวอร์ชันใหม่และกฎคัมบังที่เกี่ยวข้องได้</span><span class="sxs-lookup"><span data-stu-id="3ee79-108">This will allow you to continue your production operations while preparing the new version and related kanban rules.</span></span> 

<span data-ttu-id="3ee79-109">เมื่อต้องทำให้เวอร์ชันขั้นตอนการผลิตที่ใช้งานอยู่หมดอายุ ต้องตั้งค่าวันหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="3ee79-109">To expire an active production flow version, you need to set an expiry date.</span></span> <span data-ttu-id="3ee79-110">ในแง่นั้น การปิดใช้งานจะเหมือนกับข้อยกเว้นมากกว่ากฎ</span><span class="sxs-lookup"><span data-stu-id="3ee79-110">In that sense, deactivation is more like an exception than a rule.</span></span> 

<span data-ttu-id="3ee79-111">สำหรับขั้นตอนนี้ คุณต้องการขั้นตอนการผลิตเวอร์ชันที่สามารถปิดใช้งานได้</span><span class="sxs-lookup"><span data-stu-id="3ee79-111">For this procedure you need a production flow with a version that can be deactivated.</span></span> <span data-ttu-id="3ee79-112">อย่าลองทำสิ่งนี้ในสภาพแวดล้อมการผลิต เว้นแต่คุณจะแน่ใจ 100% ว่ารุ่นดังกล่าวล้าสมัยแล้วโดยสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="3ee79-112">Do not try this in a production environment unless you are 100% positive that the version is fully obsolete.</span></span>


## <a name="deactivate-a-production-flow-version"></a><span data-ttu-id="3ee79-113">ยกเลิกการเรียกใช้เวอร์ชันขั้นตอนการผลิต</span><span class="sxs-lookup"><span data-stu-id="3ee79-113">Deactivate a production flow version</span></span>
1. <span data-ttu-id="3ee79-114">ไปที่การควบคุมการผลิต > การตั้งค่า > ขั้นตอนการผลิตแบบ lean > ขั้นตอนการผลิต</span><span class="sxs-lookup"><span data-stu-id="3ee79-114">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="3ee79-115">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="3ee79-115">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="3ee79-116">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="3ee79-116">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="3ee79-117">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="3ee79-117">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="3ee79-118">คลิก ปิดใช้งาน</span><span class="sxs-lookup"><span data-stu-id="3ee79-118">Click Deactivate.</span></span>
    * <span data-ttu-id="3ee79-119">อย่าดำเนินการต่อ หากคุณไม่มั่นใจ 100% ว่ารุ่นของขั้นตอนการผลิตนี้ล้าสมัย </span><span class="sxs-lookup"><span data-stu-id="3ee79-119">Do not proceed if you are not 100% positive that this production flow version is obsolete.</span></span> <span data-ttu-id="3ee79-120">เมื่อคลิก ตกลง หมายความว่ากฎคัมบังที่ใช้งานอยู่ทั้งหมดจะหมดอายุลง และกิจกรรมการผลิตและการเติมสินค้าของรุ่นของขั้นตอนการผลิตนี้จะหยุดทันที</span><span class="sxs-lookup"><span data-stu-id="3ee79-120">Clicking Ok will expire all active kanban rules and put an immediate stop to all production and replenishment activities of this production flow version.</span></span>  
6. <span data-ttu-id="3ee79-121">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="3ee79-121">Click OK.</span></span>

