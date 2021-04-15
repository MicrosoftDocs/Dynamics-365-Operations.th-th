---
title: การส่งสินค้าที่ส่งคืนไปตรวจสอบอย่างละเอียด
description: ในขณะที่ลงทะเบียนสินค้าที่ส่งคืน กำหนดว่าควรจะส่งสินค้าไปตรวจสอบก่อนที่จะส่งคืนสินค้านั้นไปยังสินค้าคงคลัง หรือควรจะตัดจำหน่ายในวิธีอื่น
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WMSJournalTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bdee1ed2c7e98843e5dcfe9669e6a7c1eb11173c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810689"
---
# <a name="pass-returned-items-on-to-inspection"></a><span data-ttu-id="4d658-103">การส่งสินค้าที่ส่งคืนไปตรวจสอบอย่างละเอียด</span><span class="sxs-lookup"><span data-stu-id="4d658-103">Pass returned items on to inspection</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="4d658-104">ในขณะที่ลงทะเบียนสินค้าที่ส่งคืน คุณอาจกำหนดว่าควรจะส่งสินค้าไปตรวจสอบก่อนที่จะส่งคืนสินค้านั้นไปยังสินค้าคงคลัง หรือควรจะตัดจำหน่ายในบางกรณี</span><span class="sxs-lookup"><span data-stu-id="4d658-104">When registering a returned item, you may determine that an item should be sent for inspection before it is returned to inventory or disposed of in some other way.</span></span>

1.  <span data-ttu-id="4d658-105">คลิก **การบริหารสินค้าคงคลัง** \> **สมุดรายวัน** \> **การมาถึงของสินค้า** \> **การมาถึงของสินค้า**</span><span class="sxs-lookup"><span data-stu-id="4d658-105">Click **Inventory management** \> **Journals** \> **Item arrival** \> **Item arrival**.</span></span>
    
    <span data-ttu-id="4d658-106">\-หรือ-</span><span class="sxs-lookup"><span data-stu-id="4d658-106">\-or-</span></span>
    
    <span data-ttu-id="4d658-107">คลิก **การบริหารสินค้าคงคลัง** \> **สมุดรายวัน** \> **การมาถึงของสินค้า** \> **อินพุทการผลิต**</span><span class="sxs-lookup"><span data-stu-id="4d658-107">Click **Inventory management** \> **Journals** \> **Item arrival** \> **Production input**.</span></span>

2.  <span data-ttu-id="4d658-108">ในแบบฟอร์ม **สมุดรายวันสถานที่เก็บ** ลงทะเบียนการรับสินค้าตามปกติ</span><span class="sxs-lookup"><span data-stu-id="4d658-108">On the **Location journal** form, register the receipt of an item as usual.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="4d658-109">สำหรับข้อมูลเกี่ยวกับการลงทะเบียนการรับสินค้าส่งคืน ดู <A href="register-the-receipt-of-returned-items.md">ลงทะเบียนการรับสินค้าที่ส่งคืน</A></span><span class="sxs-lookup"><span data-stu-id="4d658-109">For information about registering the receipt of returned items, see <A href="register-the-receipt-of-returned-items.md">Register the receipt of returned items</A></span></span></P>



3.  <span data-ttu-id="4d658-110">บนแท็บ **ค่าเริ่มต้น** ในพื้นที่ **โหมดของการจัดการ** เลือกกล่อง **การบริหารการตรวจสอบสินค้า**</span><span class="sxs-lookup"><span data-stu-id="4d658-110">On the **Default values** tab, in the **Mode of handling** area, select the **Quarantine management** box.</span></span>

<span data-ttu-id="4d658-111">การทำเช่นนี้จะทำให้ระบบสร้างใบสั่งตรวจสอบสินค้า และบุคคลหรือแผนกที่ทำการตรวจสอบจะตอบสนองต่อใบสั่งนี้โดยใช้แบบฟอร์ม **ใบสั่งตรวจสอบสินค้า**</span><span class="sxs-lookup"><span data-stu-id="4d658-111">This will prompt the system to create a quarantine order, and the person or department that performs inspections will respond to this order using the **Quarantine order** form.</span></span>

## <a name="see-also"></a><span data-ttu-id="4d658-112">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="4d658-112">See also</span></span>

[<span data-ttu-id="4d658-113">การนำสินค้าที่ส่งคืนไปตรวจสอบอย่างละเอียด</span><span class="sxs-lookup"><span data-stu-id="4d658-113">Take returned items through inspection</span></span>](take-returned-items-through-inspection.md)

[<span data-ttu-id="4d658-114">การระบุวิธีการตัดจำหน่ายสินค้าที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="4d658-114">Specify how to dispose of returned items</span></span>](specify-how-to-dispose-of-returned-items.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]