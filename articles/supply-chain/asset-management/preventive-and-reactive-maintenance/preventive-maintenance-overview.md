---
title: ภาพรวมการบำรุงรักษาเชิงป้องกัน
description: หัวข้อนี้อธิบายถึงการบำรุงรักษาเชิงป้องกันในการจัดการสินทรัพย์
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3b43c795426f40cb43962976824c44a7702d91b7
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875913"
---
# <a name="preventive-maintenance-overview"></a><span data-ttu-id="4161e-103">ภาพรวมการบำรุงรักษาเชิงป้องกัน</span><span class="sxs-lookup"><span data-stu-id="4161e-103">Preventive maintenance overview</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="4161e-104">หัวข้อนี้อธิบายถึงการบำรุงรักษาเชิงป้องกันในการจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="4161e-104">This topic explains preventive maintenance in Asset Management.</span></span> <span data-ttu-id="4161e-105">การบำรุงรักษาเชิงป้องกันเป็นวินัยที่เกี่ยวข้องกับงานการบำรุงรักษาที่วางแผนไว้ เช่น บริการปกติ การสอบเทียบ และการตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="4161e-105">Preventive maintenance is a discipline involving planned maintenance jobs, for example, regular service, calibration, and inspections.</span></span> <span data-ttu-id="4161e-106">ใน **การจัดการสินทรัพย์** คุณสามารถสร้างแผนการบำรุงรักษาและตั้งค่าในสินทรัพย์และตำแหน่งที่ทำงานได้</span><span class="sxs-lookup"><span data-stu-id="4161e-106">In **Asset Management**, you can create maintenance plans and set them up on assets and functional locations.</span></span> <span data-ttu-id="4161e-107">คุณยังสามารถตั้งค่ารอบการบำรุงรักษาบนตำแหน่งที่ทำงานได้</span><span class="sxs-lookup"><span data-stu-id="4161e-107">You can also set up maintenance rounds on functional locations.</span></span> <span data-ttu-id="4161e-108">แผนการบำรุงรักษาในสินทรัพย์เปิดใช้งานโดยไม่คำนึงถึงที่ตั้งสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="4161e-108">Maintenance plans on assets are active regardless of where the asset is installed.</span></span> <span data-ttu-id="4161e-109">แผนการบำรุงรักษาและรอบการบำรุงรักษาในตำแหน่งที่ทำงาน มีผลบังคับใช้สำหรับสินทรัพย์ที่ติดตั้งอยู่ในสถานที่ในปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="4161e-109">Maintenance plans and maintenance rounds on functional location are active for the assets currently installed at the location.</span></span> <span data-ttu-id="4161e-110">แทนที่การตั้งค่าแผนการบำรุงรักษาบนสินทรัพย์หรือการตั้งค่ารอบการบำรุงรักษาในตำแหน่งที่ทำงาน คุณสามารถสร้างรอบการบำรุงรักษาที่มีสินทรัพย์หลายรายการที่คุณต้องการดำเนินการการบำรุงรักษาที่เกี่ยวข้องในกิจวัตรการทำงานเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="4161e-110">Instead of setting up maintenance plans on assets, or setting up maintenance rounds on functional locations, you can create maintenance rounds that include multiple assets on which you need to perform related types of maintenance jobs in the same work routine.</span></span> <span data-ttu-id="4161e-111">รอบการบำรุงรักษาที่สร้างขึ้นจากสินทรัพย์-แทนที่จะสร้างในตำแหน่งที่ทำงาน-หมายความว่าคุณสามารถเลือกจำนวนของสินทรัพย์สำหรับการบำรุงรักษาหนึ่งรอบ ซึ่งไม่ได้ติดตั้งบนตำแหน่งที่ทำงานเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="4161e-111">Maintenance rounds created from assets - instead of created on functional locations - means that you can select a number of assets for one maintenance round, which are not installed on the same functional location.</span></span>

<span data-ttu-id="4161e-112">แผนการบำรุงรักษาใช้สำหรับการบำรุงรักษาเชิงป้องกันและเชิงรับของสินทรัพย์แต่ละรายการ</span><span class="sxs-lookup"><span data-stu-id="4161e-112">Maintenance plans are used for preventive and reactive maintenance on individual assets.</span></span> <span data-ttu-id="4161e-113">รอบการบำรุงรักษาใช้สำหรับการบำรุงรักษาเชิงป้องกันบนกลุ่มหรือชุดของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="4161e-113">Maintenance rounds are used for preventive maintenance on a group or a set of assets.</span></span> <span data-ttu-id="4161e-114">แผนการบำรุงรักษาและรอบการบำรุงรักษาใช้สำหรับการสร้างข้อเสนอของใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="4161e-114">Maintenance plans and maintenance rounds are used for generating work order proposals.</span></span> <span data-ttu-id="4161e-115">ข้อเสนอใบสั่งงานจะถูกบันทึกเป็นรายการกำหนดการบำรุงรักษา ซึ่งสามารถรวมและแปลงเป็นใบสั่งงานได้</span><span class="sxs-lookup"><span data-stu-id="4161e-115">The work order proposals are saved as maintenance schedule lines, which can be bundled and converted into work orders.</span></span>

<span data-ttu-id="4161e-116">รูปภาพด้านล่างนี้แสดงภาพรวมของขั้นตอนการทำงานจากการสร้างแผนการบำรุงรักษาและรอบการบำรุงรักษา เพื่อสร้างใบสั่งงานสำหรับสินทรัพย์ ตามแผนการบำรุงรักษาและรอบการบำรุงรักษาเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="4161e-116">The figure below provides an overview of the work flow from creating maintenance plans and maintenance rounds to creating work orders for assets, based on those maintenance plans and maintenance rounds.</span></span>

![รูปที่ 1](media/01-preventive-maintenance.png)

