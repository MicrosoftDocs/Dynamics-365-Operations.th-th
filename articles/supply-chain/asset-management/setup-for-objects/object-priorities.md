---
title: ระดับการบริการสินทรัพย์
description: หัวข้อนี้จะอธิบายถึงระดับการบริการสินทรัพย์ในการจัดการสินทรัพย์
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f079e6899a2e3949eff5945f867472c801d9e95c
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783636"
---
# <a name="asset-service-levels"></a><span data-ttu-id="e7322-103">ระดับการบริการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="e7322-103">Asset service levels</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="e7322-104">หัวข้อนี้จะอธิบายถึงระดับการบริการสินทรัพย์ในการจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="e7322-104">This topic explains asset service levels in Asset Management.</span></span> <span data-ttu-id="e7322-105">ระดับการบริการสินทรัพย์เกี่ยวข้องกับสินทรัพย์ และจะถูกโอนย้ายไปยังคำขอการบำรุงรักษาและใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="e7322-105">Asset service levels are related to assets, and are transferred to maintenance requests and work orders.</span></span> <span data-ttu-id="e7322-106">จะมีการใช้ในการคำนวณระดับความสำคัญของใบสั่งงานในระหว่างการจัดกำหนดการใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="e7322-106">They are used to calculate the priority of work orders during work order scheduling.</span></span> <span data-ttu-id="e7322-107">ระดับการบริการสินทรัพย์สามารถเปลี่ยนแปลงได้ ถ้าจำเป็นต้องมีการเปลี่ยนแปลง</span><span class="sxs-lookup"><span data-stu-id="e7322-107">Asset service levels can be changed, if changes are required.</span></span>

<span data-ttu-id="e7322-108">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการตั้งค่าที่เกี่ยวข้องกับการคำนวณของคะแนนการจัดอันดับสำหรับการจัดกำหนดการใบสั่งงาน ดู [พารามิเตอร์การจัดการสินทรัพย์](../setup-for-objects/enterprise-asset-management-parameters.md)</span><span class="sxs-lookup"><span data-stu-id="e7322-108">For more information about the setup that is related to the calculation of rating scores for work order scheduling, see [Asset management parameters](../setup-for-objects/enterprise-asset-management-parameters.md).</span></span> <span data-ttu-id="e7322-109">คุณต้องตั้งค่าเรกคอร์ดเริ่มต้นอย่างน้อยหนึ่งเรกคอร์ดสำหรับระดับการบริการของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="e7322-109">You must set up at least one default record for the asset service level.</span></span> <span data-ttu-id="e7322-110">เรกคอร์ดเริ่มต้นนี้จะถูกใช้ ถ้าไม่พบการจับคู่อื่นระหว่างการจัดกำหนดการใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="e7322-110">This default record is used if no other match is found during work order scheduling.</span></span>

<span data-ttu-id="e7322-111">**ตัวอย่างที่ 1:** ระดับการบริการเริ่มต้นที่จะใช้ ถ้าไม่พบการจับคู่อื่น</span><span class="sxs-lookup"><span data-stu-id="e7322-111">**Example 1:** The default service level that is used if no other match is found.</span></span> <span data-ttu-id="e7322-112">ในเรกคอร์ดนี้ คุณเลือกเฉพาะระดับการบริการ</span><span class="sxs-lookup"><span data-stu-id="e7322-112">In this record, you select only a service level.</span></span>

<span data-ttu-id="e7322-113">**ตัวอย่างที่ 2:** ระดับการบริการสูงที่ใช้ในการจัดกำหนดการงานสำหรับเครื่องยนต์รถบรรทุก Volvo</span><span class="sxs-lookup"><span data-stu-id="e7322-113">**Example 2:** A high service level that is used to schedule jobs for a Volvo truck engine.</span></span> <span data-ttu-id="e7322-114">ในเรกคอร์ดนี้ คุณเลือกชนิดของสินทรัพย์ที่เกี่ยวข้อง (เช่น **เครื่องยนต์รถบรรทุก**) ผู้ผลิต (**Volvo**) และระดับการบริการ</span><span class="sxs-lookup"><span data-stu-id="e7322-114">In this record, you select a relevant asset type (such as **Truck Engine**), a manufacturer (**Volvo**), and a service level.</span></span>

## <a name="set-up-asset-service-levels"></a><span data-ttu-id="e7322-115">ตั้งค่าระดับการบริการของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="e7322-115">Set up asset service levels</span></span>

1. <span data-ttu-id="e7322-116">เลือก **การจัดการสินทรัพย์** \> **การตั้งค่า** \> **ระดับการบริการสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="e7322-116">Select **Asset management** \> **Setup** \> **Asset service levels**.</span></span>
2. <span data-ttu-id="e7322-117">เลือก **สร้าง** เพื่อสร้างเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="e7322-117">Select **New** to create a record.</span></span>
3. <span data-ttu-id="e7322-118">โดยขึ้นอยู่กับระดับของรายละเอียดที่จำเป็นสำหรับระดับการบริการของสินทรัพย์ ทำให้การเลือกในฟิลด์ **ตำแหน่งที่ทำงาน** **ชนิดสินทรัพย์** **ผู้ผลิต** **แบบจำลอง** **สินทรัพย์** **ชนิดใบสั่งงาน** และ **ระดับการบริการ** มีความเกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="e7322-118">Depending on the detail level that is required for the asset service level, make relevant selections in the **Functional location**, **Asset type**, **Manufacturer**, **Model**, **Asset**, **Work order type**, and **Service level** fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e7322-119">เมื่อมีการใช้ระดับการบริการของสินทรัพย์สำหรับคำขอการบำรุงรักษาและใบสั่งงาน การจัดการสินทรัพย์จะผ่านเรกคอร์ดของระดับการบริการของสินทรัพย์ทั้งหมด เพื่อตรวจสอบการจับคู่ที่เป็นไปได้</span><span class="sxs-lookup"><span data-stu-id="e7322-119">When the asset service level is used for maintenance requests and work orders, Asset Management goes through all asset service level records to check for a possible match.</span></span> <span data-ttu-id="e7322-120">ซึ่งจะตรวจสอบชุดที่เฉพาะเจาะจงมากที่สุดก่อน</span><span class="sxs-lookup"><span data-stu-id="e7322-120">It always checks the most specific combination first.</span></span> <span data-ttu-id="e7322-121">กล่าวคือ อันดับแรกการจัดการสินทรัพย์จะตรวจสอบการจับคู่สำหรับฟิลด์ **ชนิดใบสั่งงาน**</span><span class="sxs-lookup"><span data-stu-id="e7322-121">In other words, Asset Management first checks for a match for the **Work order type** field.</span></span> <span data-ttu-id="e7322-122">ถ้าไม่พบการจับคู่ จะตรวจสอบการจับคู่สำหรับฟิลด์ **สินทรัพย์** เป็นต้น</span><span class="sxs-lookup"><span data-stu-id="e7322-122">If no match is found, it checks for a match for the **Asset** field, and so on.</span></span> <span data-ttu-id="e7322-123">ดังที่คุณสามารถดูได้ในโครงร่างของหน้า **ระดับการบริการของสินทรัพย์** ลักษณะการทำงานนี้หมายความว่า การค้นหาชุดที่เฉพาะเจาะจงมากที่สุด การจัดการสินทรัพย์จะตรวจสอบเรกคอร์ดแต่ละรายการจากขวาไปซ้ายสำหรับการจับคู่</span><span class="sxs-lookup"><span data-stu-id="e7322-123">As you can see in the layout of the **Asset service levels** page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match.</span></span> <span data-ttu-id="e7322-124">ถ้าไม่พบการจับคู่ จะมีการใช้เรกคอร์ดข้อมูลเริ่มต้นที่ไม่มีการเลือกในฟิลด์เหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="e7322-124">If no match is found, the default record that has no selections in those fields is used.</span></span>

4. <span data-ttu-id="e7322-125">ในฟิลด์ **ระดับการบริการ** ให้เลือกหมายเลขที่บ่งชี้ระดับการบริการ (ระดับความสำคัญ)</span><span class="sxs-lookup"><span data-stu-id="e7322-125">In the **Service level** field, select a number that indicates the service level (priority).</span></span>


> [!NOTE]
> <span data-ttu-id="e7322-126">ถ้าคุณเปลี่ยนเรกคอร์ดระดับการบริการของสินทรัพย์บนหน้า **ระดับการบริการของสินทรัพย์** หลังจากที่คุณได้ใช้ในใบสั่งงานแล้ว ระดับการบริการในคำขอการบำรุงรักษาและใบสั่งงานจะไม่ได้รับการปรับปรุงให้สอดคล้องกัน</span><span class="sxs-lookup"><span data-stu-id="e7322-126">If you change an asset service level record on the **Asset service levels** page after you've already used it on a work order, the service level on maintenance requests and work orders isn't updated accordingly.</span></span>
