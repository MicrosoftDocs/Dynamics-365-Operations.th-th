---
title: การตั้งค่าคลังสินค้าสำหรับใบสั่งโอนย้าย
description: หัวข้อนี้อธิบายวิธีการตั้งค่าคลังสินค้าสำหรับใบสั่งโอนย้าย
author: Mirzaab
manager: tfehr
ms.date: 01/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: aa5786df72f87da992f1020bbaaa1c2185adf043
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216727"
---
# <a name="set-up-warehouses-for-transfer-orders"></a><span data-ttu-id="19e71-103">การตั้งค่าคลังสินค้าสำหรับใบสั่งโอนย้าย</span><span class="sxs-lookup"><span data-stu-id="19e71-103">Set up warehouses for transfer orders</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="19e71-104">คุณสามารถใช้ระดับคลังสินค้าเพื่อสร้างลำดับชั้นที่สนับสนุนใบสั่งโอนย้ายระหว่างคลังสินค้าได้ </span><span class="sxs-lookup"><span data-stu-id="19e71-104">You can use warehouse levels to create a hierarchy that supports transfer orders between warehouses.</span></span> <span data-ttu-id="19e71-105">การวางแผนหลักจะใช้การตั้งค่านี้ เพื่อคำนวณความต้องการสินค้าที่ระดับคลังสินค้าแต่ละระดับและสร้างแผนการใบสั่งย้ายจากคลังสินค้าต้นทางที่กำหนดเพื่อตอบสนองแผนการใบสั่งเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="19e71-105">Based on this setup, master scheduling calculates item requirements at the individual warehouse level and generates planned transfer orders from an assigned source warehouse to fulfill them.</span></span>

1.  <span data-ttu-id="19e71-106">คลิก **การบริหารสินค้าคงคลัง > การตั้งค่า > แบ่งสินค้าคงคลัง > คลังสินค้า**.</span><span class="sxs-lookup"><span data-stu-id="19e71-106">Click **Inventory management > Setup > Inventory breakdown > Warehouses**.</span></span>

2.  <span data-ttu-id="19e71-107">เลือกคลังสินค้าที่คุณต้องการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="19e71-107">Select the warehouse that you want to refill.</span></span>

3.  <span data-ttu-id="19e71-108">ในแท็บด่วน **การวางแผนหลัก** เลือกกล่องกาเครื่องหมาย **การเพิ่มสินค้า**</span><span class="sxs-lookup"><span data-stu-id="19e71-108">On the **Master planning** FastTab, select the **Refilling** check box.</span></span>

4.  <span data-ttu-id="19e71-109">ในฟิลด์ **คลังสินค้าหลัก** ให้เลือกคลังสินค้าที่ต้องการกำหนดเป็นคลังสินค้าเติม</span><span class="sxs-lookup"><span data-stu-id="19e71-109">In the **Main warehouse** field, select the warehouse that you want to assign as the refilling warehouse.</span></span> <span data-ttu-id="19e71-110">การวางแผนหลักจะคำนวณความต้องการโอนย้ายสำหรับคลังสินค้าที่เลือกและสร้างแผนการใบสั่งย้ายจาก **คลังสินค้าหลัก** ที่กำหนด</span><span class="sxs-lookup"><span data-stu-id="19e71-110">Master scheduling calculates a transfer requirement for the selected warehouse and generates a planned transfer order from the assigned **Main warehouse**.</span></span>
   
    > [!NOTE]
    > <P><span data-ttu-id="19e71-111">ถ้าคุณยกเลิกการเลือกกล่องกาเครื่องหมาย <STRONG>การเพิ่มสินค้า</STRONG> คลังสินค้าที่เลือกจะได้รับการกำหนดระดับคลังสินค้าโดยเกี่ยวข้องกับ <STRONG>คลังสินค้าหลัก</STRONG> แต่ <STRONG>คลังสินค้าหลัก</STRONG> จะไม่ได้รับการตั้งค่าเป็นคลังสินค้าสำหรับการเติมสินค้า</span><span class="sxs-lookup"><span data-stu-id="19e71-111">If you clear the <STRONG>Refilling</STRONG> check box, the selected warehouse is assigned a warehouse level in regard to the <STRONG>Main warehouse</STRONG>, but the <STRONG>Main warehouse</STRONG> is not set up as a refilling warehouse.</span></span></P>

5.  <span data-ttu-id="19e71-112">ปิดหน้าเพื่อใช้การตั้งค่าใหม่</span><span class="sxs-lookup"><span data-stu-id="19e71-112">Close the page to apply the new setup.</span></span>


> [!TIP]
> <P><span data-ttu-id="19e71-113">ถ้าคุณต้องการกำหนดคลังสินค้าสำหรับการเติมสินค้า คุณต้องตั้งค่าคลังสินค้าเป็นมิติการจัดเก็บในหน้า <STRONG>กลุ่มมิติการจัดเก็บ</STRONG></span><span class="sxs-lookup"><span data-stu-id="19e71-113">If you want to assign a warehouse for refilling, you must first set up the warehouse as a storage dimension on the <STRONG>Storage dimension groups</STRONG> page.</span></span> <span data-ttu-id="19e71-114">บนหน้านี้ เลือกฟิลด์ <STRONG>ใช้งาน</STRONG> และฟิลด์ <STRONG>วางแผนความครอบคลุมโดยเรียงตามมิติ</STRONG> สำหรับคลังสินค้า</span><span class="sxs-lookup"><span data-stu-id="19e71-114">On this page, select the <STRONG>Active</STRONG> field and the <STRONG>Coverage plan by dimension</STRONG> field for the warehouse.</span></span></P>

## <a name="set-up-transport-lead-time"></a><span data-ttu-id="19e71-115">ตั้งค่าระยะเวลารอคอยสินค้าการขนส่ง</span><span class="sxs-lookup"><span data-stu-id="19e71-115">Set up transport lead time</span></span>

<span data-ttu-id="19e71-116">คุณต้องตั้งค่าระยะเวลารอคอยสินค้าการขนส่งระหว่างคลังสินค้าบนหน้า **จำนวนวันที่ใช้ในการขนส่ง**</span><span class="sxs-lookup"><span data-stu-id="19e71-116">You must also set up the transport lead time between the warehouses on the **Transport days** page.</span></span> 
1. <span data-ttu-id="19e71-117">ไปยัง **การบริหารสินค้าคงคลัง > การตั้งค่า > การกระจาย > จำนวนวันที่ใช้ในการขนส่ง**</span><span class="sxs-lookup"><span data-stu-id="19e71-117">Go to **Inventory management > Setup > Distribution > Transport days**.</span></span>
2. <span data-ttu-id="19e71-118">ในฟิลด์ **จุดรับสินค้า** เลือก **คลังสินค้า**</span><span class="sxs-lookup"><span data-stu-id="19e71-118">In the **Receiving point** field, select **warehouse**.</span></span>
3. <span data-ttu-id="19e71-119">เลือก **คลังสินค้าที่จัดส่ง**, **คลังสินค้าที่รับเข้า** และ **จำนวนวันที่ใช้ในการขนส่ง**</span><span class="sxs-lookup"><span data-stu-id="19e71-119">Select the **Shipping warehouse**, **Receiving warehouse**, and **Transport days**.</span></span> 
4. <span data-ttu-id="19e71-120">(ไม่จำเป็น) คุณยังสามารถตั้งค่าเวลาที่ใช้ในการขนส่งโดยขึ้นอยู่กับวิธีการจัดส่ง ภายใต้แท็บ **จำนวนวันที่ใช้ในการส่งต่อวิธีการจัดส่ง**</span><span class="sxs-lookup"><span data-stu-id="19e71-120">(Optional) You can also set transport time, depending on the mode of delivery, under the **Transport days per mode of delivery** tab.</span></span>
