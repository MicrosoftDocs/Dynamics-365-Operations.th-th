---
title: ลงรายการบัญชีสมุดรายวันการมาถึงสำหรับผลิตภัณฑ์ที่ส่งคืน
description: ลงรายการบัญชีสมุดรายวันการมาถึงสำหรับผลิตภัณฑ์ที่ส่งคืน
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverview
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e07542a369506b810704012bd1b07557b79f50d7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4438659"
---
# <a name="post-arrival-journal-for-returned-products"></a><span data-ttu-id="94321-103">ลงรายการบัญชีสมุดรายวันการมาถึงสำหรับผลิตภัณฑ์ที่ส่งคืน</span><span class="sxs-lookup"><span data-stu-id="94321-103">Post arrival journal for returned products</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="94321-104">ในการประมวลผลการส่งคืน อันดับแรกให้ตรวจสอบปริมาณการส่งคืน อัพเดตฟิลด์ปริมาณในสมุดรายวันการมาถึงของสินค้า</span><span class="sxs-lookup"><span data-stu-id="94321-104">To process a return, first validate the return quantity, update the quantity field in the item arrival journal.</span></span> <span data-ttu-id="94321-105">จากนั้นเลือกรหัสการโอนการครอบครอง หรือบ่งชี้ว่าสินค้าที่ส่งคืนต้องถูกตรวจสอบ</span><span class="sxs-lookup"><span data-stu-id="94321-105">Then select a disposition code or indicate that the returned items have to be inspected.</span></span> <span data-ttu-id="94321-106">หลังจากทำขั้นตอนเหล่านี้เสร็จสมบูรณ์แล้ว คุณสามารถลงรายการบัญชีสมุดรายวันการมาถึงของสินค้าสำหรับใบสั่งส่งคืนสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="94321-106">After completing these steps, you can post the item arrival journal for the return order.</span></span>

1.  <span data-ttu-id="94321-107">คลิก **การบริหารสินค้าคงคลัง** \> **งานประจำงวด** \> **ภาพรวมของการมาถึง**</span><span class="sxs-lookup"><span data-stu-id="94321-107">Click **Inventory management** \> **Periodic** \> **Arrival overview**.</span></span>

2.  <span data-ttu-id="94321-108">ในตัวกรอง **ชื่อการตั้งค่า** เลือก **ใบสั่งส่งคืน**</span><span class="sxs-lookup"><span data-stu-id="94321-108">In the **Setup name** filter, select **Return order**.</span></span>

3.  <span data-ttu-id="94321-109">ถ้ารายการของการรับสินค้ายาว ให้ใช้ฟิลด์ในพื้นที่ **ช่วง** เพื่อทำให้รายการสั้นลง</span><span class="sxs-lookup"><span data-stu-id="94321-109">If the list of receipts is long, use the fields in the **Range** area to narrow the list.</span></span>

4.  <span data-ttu-id="94321-110">ค้นหารายการของใบสั่งส่งคืนสินค้าที่คุณต้องการลงรายการบัญชี เลือกกล่อง **เลือกสำหรับการมาถึง** ของรายการนั้น แล้วคลิก **เริ่มต้นการมาถึง**</span><span class="sxs-lookup"><span data-stu-id="94321-110">Locate the line of the return order that you want to post, select its **Select for arrival** box, and then click **Start arrival**.</span></span>

5.  <span data-ttu-id="94321-111">คลิก **สมุดรายวัน** \> **แสดงการมาถึงจากใบเสร็จรับเงิน** เพื่อเปิดแบบฟอร์ม **สมุดรายวันสถานที่เก็บ**</span><span class="sxs-lookup"><span data-stu-id="94321-111">Click **Journals** \> **Show arrivals from receipts** to open the **Location journal** form.</span></span>
    

    > [!TIP]
    > <P><span data-ttu-id="94321-112">ถ้าต้องการดูข้อมูลโดยละเอียด ให้เลือกสมุดรายวัน แล้วคลิก <STRONG>รายการ</STRONG></span><span class="sxs-lookup"><span data-stu-id="94321-112">To view detailed information, select a journal, and then click <STRONG>Lines</STRONG>.</span></span></P>


6.  <span data-ttu-id="94321-113">ทำการอัพเดตที่จำเป็นใดๆ แล้วคลิก **ลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="94321-113">Make any necessary updates, and then click **Post**.</span></span>

<span data-ttu-id="94321-114">หลังจากลงรายการบัญชีสมุดรายวันแล้ว ระบบจะลงทะเบียนสินค้าที่ส่งคืนในสินค้าคงคลัง และแบบฟอร์ม **ใบสั่งส่งคืนสินค้า** บ่งชี้ว่าสินค้าได้มาถึงที่คลังสินค้าแล้ว</span><span class="sxs-lookup"><span data-stu-id="94321-114">After the journal is posted, the returned items are registered in inventory, and the **Return orders** form indicates that the items have arrived at the warehouse.</span></span>

## <a name="see-also"></a><span data-ttu-id="94321-115">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="94321-115">See also</span></span>

<span data-ttu-id="94321-116">[สมุดรายวันสถานที่เก็บ (แบบฟอร์ม)](https://technet.microsoft.com/library/aa584822\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="94321-116">[Location journal (form)](https://technet.microsoft.com/library/aa584822\(v=ax.60\))</span></span>

  


