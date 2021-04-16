---
title: สร้างกฎคัมบังใหม่โดยทำซ้ำกฎคัมบังที่มีอยู่
description: 'ขั้นตอนนี้มุ่งเน้นการสร้างการทำซ้ำของกฎคัมบังที่มีอยู่ '
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d80bf0318234f858e51fb461894238894e01717c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829077"
---
# <a name="create-a-new-kanban-rule-by-duplicating-an-existing-kanban-rule"></a><span data-ttu-id="349e6-103">สร้างกฎคัมบังใหม่โดยทำซ้ำกฎคัมบังที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="349e6-103">Create a new kanban rule by duplicating an existing kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="349e6-104">ขั้นตอนนี้มุ่งเน้นการสร้างการทำซ้ำของกฎคัมบังที่มีอยู่ </span><span class="sxs-lookup"><span data-stu-id="349e6-104">This procedure focuses on creating a duplicate of an existing kanban rule.</span></span> <span data-ttu-id="349e6-105">สิ่งนี้มีประโยชน์ถ้าคุณต้องการจะสร้างกฎคัมบังใหม่โดยอาศัยกฎคัมบังที่มีอยู่ </span><span class="sxs-lookup"><span data-stu-id="349e6-105">This is useful if you want to create new kanban rules based on existing kanban rules.</span></span> <span data-ttu-id="349e6-106">ข้อมูลบริษัทสาธิตที่ใช้ในการสร้างกระบวนงานนี้คือ USMF</span><span class="sxs-lookup"><span data-stu-id="349e6-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="349e6-107">ขั้นตอนนี้มีไว้สำหรับวิศวกรกระบวนการหรือผู้จัดการสตรีมค่าตามที่พวกเขาจัดเตรียมการผลิตสำหรับผลิตภัณฑ์ใหม่หรือผลิตภัณฑ์ปรับเปลี่ยน</span><span class="sxs-lookup"><span data-stu-id="349e6-107">This procedure is intended for the process engineer or the value stream manager as they prepare production for a changed production flow or a new replenishment rule.</span></span>


## <a name="select-a-kanban-rule"></a><span data-ttu-id="349e6-108">เลือกกฎคัมบัง</span><span class="sxs-lookup"><span data-stu-id="349e6-108">Select a kanban rule</span></span>
1. <span data-ttu-id="349e6-109">ไปที่กฎคัมบัง</span><span class="sxs-lookup"><span data-stu-id="349e6-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="349e6-110">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="349e6-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="349e6-111">เลือกเหตุการณ์กฎคัมบัง 000017 สำหรับ M0006</span><span class="sxs-lookup"><span data-stu-id="349e6-111">Select kanban rule 000017 for Product M0006.</span></span>  

## <a name="duplicate-a-kanban-rule"></a><span data-ttu-id="349e6-112">ทำซ้ำกฎคัมบัง</span><span class="sxs-lookup"><span data-stu-id="349e6-112">Duplicate a kanban rule</span></span>
1. <span data-ttu-id="349e6-113">คลิกทำซ้ำกฎคัมบัง</span><span class="sxs-lookup"><span data-stu-id="349e6-113">Click Duplicate kanban rule.</span></span>
    * <span data-ttu-id="349e6-114">เมื่อทำซ้ำกฎคัมบัง เป็นไปได้ที่จะเปลี่ยนชนิด วัน กิจกรรม และการเลือกผลิตภัณฑ์ </span><span class="sxs-lookup"><span data-stu-id="349e6-114">When duplicating a kanban rule, it is possible to change type, dates, activities, and the product selection.</span></span> <span data-ttu-id="349e6-115">เปลี่ยนผลิตภัณฑ์สำหรับขั้นตอนนี้ในขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="349e6-115">Change the product for this procedure in the next step.</span></span>  
2. <span data-ttu-id="349e6-116">ในฟิลด์ผลิตภัณฑ์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="349e6-116">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="349e6-117">เลือก M0007</span><span class="sxs-lookup"><span data-stu-id="349e6-117">Select M0007.</span></span>  
3. <span data-ttu-id="349e6-118">คลิก ตกลง</span><span class="sxs-lookup"><span data-stu-id="349e6-118">Click OK.</span></span>
    * <span data-ttu-id="349e6-119">โปรดทราบว่ามีการสร้างซ้ำของกฎคัมบัง 000017</span><span class="sxs-lookup"><span data-stu-id="349e6-119">Note that a duplicate of kanban rule 000017 is created.</span></span>    



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]