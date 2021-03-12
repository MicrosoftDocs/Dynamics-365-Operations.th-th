---
title: กำหนดวันหมดอายุสำหรับรุ่นขั้นตอนการผลิต
description: 'เมื่อต้องการสิ้นสุดการมีผลบังคับใช้และการประมวลผลรุ่นของขั้นตอนการผลิตในวันที่กำหนด หรือเมื่อต้องการวางแผนการเปลี่ยนรุ่นที่ใช้งานอยู่เป็นรุ่นใหม่ คุณจะต้องกำหนดวันหมดอายุของรุ่น '
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a595ca4ff9f6753631303b656d56735320a22a69
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975096"
---
# <a name="define-an-expiry-date-for-a-production-flow-version"></a><span data-ttu-id="f7730-103">กำหนดวันหมดอายุสำหรับรุ่นขั้นตอนการผลิต</span><span class="sxs-lookup"><span data-stu-id="f7730-103">Define an expiry date for a production flow version</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f7730-104">เมื่อต้องการสิ้นสุดการมีผลบังคับใช้และการประมวลผลรุ่นของขั้นตอนการผลิตในวันที่กำหนด หรือเมื่อต้องการวางแผนการเปลี่ยนรุ่นที่ใช้งานอยู่เป็นรุ่นใหม่ คุณจะต้องกำหนดวันหมดอายุของรุ่น </span><span class="sxs-lookup"><span data-stu-id="f7730-104">To end the validity and the processing of a production flow version on a given date, or to plan replacement of an active version with a new version, you have to set an expiry date on the version.</span></span> <span data-ttu-id="f7730-105">โดยที่คุณไม่จำเป็นต้องปิดใช้งานรุ่นนั้นๆ</span><span class="sxs-lookup"><span data-stu-id="f7730-105">It is not necessary to deactivate the version.</span></span>


## <a name="set-an-expiration-date-to-end-a-production-flow-version"></a><span data-ttu-id="f7730-106">กำหนดวันหมดอายุเพื่อสิ้นสุดรุ่นของขั้นตอนการผลิต</span><span class="sxs-lookup"><span data-stu-id="f7730-106">Set an expiration date to end a production flow version</span></span>
1. <span data-ttu-id="f7730-107">ไปที่การควบคุมการผลิต > การตั้งค่า > ขั้นตอนการผลิตแบบ lean > ขั้นตอนการผลิต</span><span class="sxs-lookup"><span data-stu-id="f7730-107">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="f7730-108">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="f7730-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f7730-109">เลือกขั้นตอนการผลิตที่มีรุ่นที่กำหนดแล้ว</span><span class="sxs-lookup"><span data-stu-id="f7730-109">Select any production flow that has a version that is already defined.</span></span>  
3. <span data-ttu-id="f7730-110">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f7730-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="f7730-111">คลิก แก้ไข</span><span class="sxs-lookup"><span data-stu-id="f7730-111">Click Edit.</span></span>
5. <span data-ttu-id="f7730-112">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="f7730-112">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="f7730-113">ในฟิลด์วันหมดอายุ ให้ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="f7730-113">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="f7730-114">สำหรับวันหมดอายุ รุ่นใหม่จะไม่เริ่มต้นหรือกลายเป็น เรียกใช้แล้ว </span><span class="sxs-lookup"><span data-stu-id="f7730-114">For the expiration date, a new version will not start or become activated.</span></span> <span data-ttu-id="f7730-115">จะไม่สามารถสร้างหรือเริ่มต้นงานสำหรับขั้นตอนการผลิตนี้ได้อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="f7730-115">It will also no longer be possible to create or start jobs for this production flow.</span></span> <span data-ttu-id="f7730-116">คุณยังคงสามารถทำงานที่เริ่มต้นแล้วให้เสร็จสิ้นได้หลังจากวันหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="f7730-116">You can still complete started jobs after the expiration date.</span></span>  

