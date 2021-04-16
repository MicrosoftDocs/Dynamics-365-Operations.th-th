---
title: ตั้งค่ารหัสการโอนการครอบครอง
description: คุณสามารถตั้งค่ารหัสการโอนการครอบครอง เพื่อระบุวิธีการประมวลผลสินค้าที่ถูกส่งคืนโดยลูกค้าได้
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReturnDispositionCode
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c5049c6d1fc5fcfae3bb6c7da1dd8d078ce9c33e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835785"
---
# <a name="set-up-disposition-codes"></a><span data-ttu-id="4a08d-103">ตั้งค่ารหัสการโอนการครอบครอง</span><span class="sxs-lookup"><span data-stu-id="4a08d-103">Set up disposition codes</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="4a08d-104">คุณสามารถตั้งค่ารหัสการโอนการครอบครอง เพื่อระบุวิธีการประมวลผลสินค้าที่ถูกส่งคืนโดยลูกค้าได้</span><span class="sxs-lookup"><span data-stu-id="4a08d-104">You can set up disposition codes to specify how to process an item that is returned by a customer.</span></span> <span data-ttu-id="4a08d-105">ตัวอย่างเช่น สร้างรหัสการโอนการครอบครองที่ชื่อว่า **ซ่อมแซมและส่งคืน** เพื่อบ่งชี้ว่า สินค้าที่ส่งคืนจะถูกซ่อมแซม แล้วถูกส่งคืนให้แก่ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="4a08d-105">For example, create a disposition code named **Repair and return** to indicate that the returned item will be repaired and then returned to the customer.</span></span> <span data-ttu-id="4a08d-106">สำหรับตัวอย่างเพิ่มเติมเกี่ยวกับรหัสการโอนการครอบครองที่ถูกใช้โดยทั่วไปสำหรับสินค้าที่ถูกส่งคืนโดยลูกค้า โปรดดู [Specify how to dispose of returned items](specify-how-to-dispose-of-returned-items.md).</span><span class="sxs-lookup"><span data-stu-id="4a08d-106">For more examples of disposition codes that are typically used for items that are returned by customers, see [Specify how to dispose of returned items](specify-how-to-dispose-of-returned-items.md).</span></span>

<span data-ttu-id="4a08d-107">นอกจากนี้ คุณยังสามารถตั้งค่ารหัสเหตุผลเพื่อช่วยอธิบายว่า เพราะเหตุใดจึงมีการส่งคืนสินค้า</span><span class="sxs-lookup"><span data-stu-id="4a08d-107">You can also set up a reason code to help explain why an item was returned.</span></span> <span data-ttu-id="4a08d-108">สำหรับข้อมูลเพิ่มเติมเกี่ยวกับรหัสเหตุผล ให้ดูที่ [ตั้งค่ารหัสเหตุผลในการส่งคืน](set-up-return-reason-code.md)</span><span class="sxs-lookup"><span data-stu-id="4a08d-108">For more information about reason codes, see [Set up return reason codes](set-up-return-reason-code.md).</span></span>

1.  <span data-ttu-id="4a08d-109">ไปที่ **การขายและการตลาด** \> **ตั้งค่า** \> **ใบสั่งขาย** \> **การส่งคืนสินค้า** \> **รหัสการโอนการครอบครอง**</span><span class="sxs-lookup"><span data-stu-id="4a08d-109">Go to **Sales and marketing** \> **Setup** \> **Sales orders** \> **Returns** \> **Disposition codes**.</span></span>

2.  <span data-ttu-id="4a08d-110">เลือก **สร้าง** เพื่อสร้างรหัสการโอนการครอบครองใหม่</span><span class="sxs-lookup"><span data-stu-id="4a08d-110">Select **New** to create a new disposition code.</span></span>

3.  <span data-ttu-id="4a08d-111">ป้อนชื่อที่เป็นคำอธิบายที่ไม่ซ้ำ เลือกการดำเนินการ และป้อนคำอธิบายสำหรับรหัสการโอนการครอบครอง</span><span class="sxs-lookup"><span data-stu-id="4a08d-111">Enter a unique, descriptive name, select an action, and enter a description for the disposition code.</span></span>

4.  <span data-ttu-id="4a08d-112">ถ้าคุณต้องการเชื่อมโยงค่าธรรมเนียมของลูกค้าใดๆ เข้ากับรหัสการโอนการครอบครองนี้ ให้เลือกปุ่ม **ค่าธรรมเนียม** เพื่อเปิดแบบฟอร์ม **ตั้งค่าค่าธรรมเนียม**</span><span class="sxs-lookup"><span data-stu-id="4a08d-112">If you want to associate any customer charges with this disposition code, select the **Charges** button to open the **Set up charges** form.</span></span>

5.  <span data-ttu-id="4a08d-113">ถ้าคุณต้องการกำหนดรหัสภายนอกเพื่อจับคู่กับรหัสการโอนการครอบครองของบริษัทของคุณเอง ให้เลือกปุ่ม **รหัสภายนอก** เพื่อเปิดแบบฟอร์ม **รหัสภายนอก**</span><span class="sxs-lookup"><span data-stu-id="4a08d-113">If you want to define any external codes to match with the company's own disposition codes, select the **External codes** button to open the **External codes** form.</span></span>

## <a name="see-also"></a><span data-ttu-id="4a08d-114">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="4a08d-114">See also</span></span>

[<span data-ttu-id="4a08d-115">ภาพรวมของการส่งคืนของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="4a08d-115">Customer returns overview</span></span>](disposition-and-return-reason-codes.md)

<span data-ttu-id="4a08d-116">[รหัสการจัดการ (แบบฟอร์ม)](https://technet.microsoft.com/library/hh597113\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="4a08d-116">[Disposition codes (form)](https://technet.microsoft.com/library/hh597113\(v=ax.60\))</span></span>

<span data-ttu-id="4a08d-117">[ค่าธรรมเนียมอัตโนมัติ (แบบฟอร์ม)](https://technet.microsoft.com/library/aa582856\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="4a08d-117">[Auto charges (form)](https://technet.microsoft.com/library/aa582856\(v=ax.60\))</span></span>

<span data-ttu-id="4a08d-118">[รหัสภายนอก (แบบฟอร์ม)](https://technet.microsoft.com/library/aa583814\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="4a08d-118">[External codes (form)](https://technet.microsoft.com/library/aa583814\(v=ax.60\))</span></span>

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]