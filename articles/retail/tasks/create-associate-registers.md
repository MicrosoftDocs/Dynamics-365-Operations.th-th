--- 
title: " สร้างและเชื่อมโยงการลงทะเบียน"
description: "กระบวนงานนี้อธิบายวิธีการสร้างเครื่องบันทึกเงินสดการขายหน้าร้าน (POS) "
author: rubencdelgado
manager: AnnBe
ms.date: 10/05/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6a95019e50bcc060165dab3e6aa2b3ca8a897bf3
ms.contentlocale: th-th
ms.lasthandoff: 09/29/2017

---
# <a name="create-and-associate-registers"></a><span data-ttu-id="0a8ee-103"> สร้างและเชื่อมโยงการลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="0a8ee-103">Create and associate registers</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="0a8ee-104">กระบวนงานนี้อธิบายวิธีการสร้างเครื่องบันทึกเงินสดการขายหน้าร้าน (POS) </span><span class="sxs-lookup"><span data-stu-id="0a8ee-104">This procedure demonstrates how to create a point of sale (POS) register.</span></span> <span data-ttu-id="0a8ee-105">กระบวนงานนี้ใช้ข้อมูลบริษัทสาธิต USRT</span><span class="sxs-lookup"><span data-stu-id="0a8ee-105">This procedure uses the demo data company USRT.</span></span>

1. <span data-ttu-id="0a8ee-106">ไปยังการขายปลีกและการค้า > การตั้งค่าช่องทาง > การตั้งค่า POS > การลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="0a8ee-106">Go to Retail and commerce > Channel setup > POS setup > Registers.</span></span>
2. <span data-ttu-id="0a8ee-107">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="0a8ee-107">Click New.</span></span>
3. <span data-ttu-id="0a8ee-108">ในฟิลด์หมายเลขเครื่องบันทึกเงินสด ให้พิมพ์รหัสสำหรับเครื่องบันทึกเงินสดใหม่</span><span class="sxs-lookup"><span data-stu-id="0a8ee-108">In the Register number field, type an ID for the new register.</span></span>
    * <span data-ttu-id="0a8ee-109">โดยทั่วไปรหัสเครื่องบันทึกเงินสดจะประกอบด้วยรหัสที่ช่วยในการแม็ปเครื่องบันทึกเงินสดให้กับร้านค้าที่เป็นเจ้าของ และสถานที่ภายในร้านค้า</span><span class="sxs-lookup"><span data-stu-id="0a8ee-109">The register ID typically includes codes that help map the register to the store to which it belongs, and the location within the store.</span></span>  
4. <span data-ttu-id="0a8ee-110">ในฟิลด์ชื่อ ให้พิมพ์ชื่อที่เป็นคำอธิบายสำหรับเครื่องบันทึกเงินสด</span><span class="sxs-lookup"><span data-stu-id="0a8ee-110">In the Name field, type a descriptive name for the register..</span></span>
5. <span data-ttu-id="0a8ee-111">ในฟิลด์หมายเลขร้านค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="0a8ee-111">In the Store number field, enter or select a value.</span></span>
6. <span data-ttu-id="0a8ee-112">ในฟิลด์โพรไฟล์ฮาร์ดแวร์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="0a8ee-112">In the Hardware profile field, enter or select a value.</span></span>
    * <span data-ttu-id="0a8ee-113">โพรไฟล์ฮาร์ดแวร์จะใช้เพื่อระบุอุปกรณ์ต่อพ่วงขายปลีกที่จะเชื่อมต่อกับเครื่องบันทึกเงินสด เช่น ลิ้นชักเงินสดและเครื่องพิมพ์ใบเสร็จ</span><span class="sxs-lookup"><span data-stu-id="0a8ee-113">Hardware profiles are used to specify the retail peripherals that will be connected to the register, such as cash drawer and receipt printer.</span></span>  
7. <span data-ttu-id="0a8ee-114">ในฟิลด์โพรไฟล์ภาพ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="0a8ee-114">In the Visual profile field, enter or select a value.</span></span>
    * <span data-ttu-id="0a8ee-115">โพรไฟล์ภาพจะใช้เพื่อระบุรูปภาพที่ใช้ในพื้นหลัง POS และหน้าล็อกอิน รวมทั้งชุดรูปแบบสำหรับ POS</span><span class="sxs-lookup"><span data-stu-id="0a8ee-115">Visual profiles are used to specify the images used in the POS background and login page as well as themes for the POS.</span></span>  
8. <span data-ttu-id="0a8ee-116">ในฟิลด์หมายเลขเครื่องบันทึกเงินสด EFT POS ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="0a8ee-116">In the EFT POS register number field, type a value.</span></span>
    * <span data-ttu-id="0a8ee-117">หมายเลขเครื่องบันทึกเงินสด EFT POS จะใช้เพื่อแจ้งตัวประมวลผลการชำระเงินว่าเทอร์มินัลการชำระเงินใดจะส่งคำขอตรวจสอบ </span><span class="sxs-lookup"><span data-stu-id="0a8ee-117">The EFT POS register number is used to inform the payment processor which payment terminal is sending authorization requests.</span></span> <span data-ttu-id="0a8ee-118">ค่านี้มักเรียกว่า "รหัสเทอร์มินัล" หรือ "TID" </span><span class="sxs-lookup"><span data-stu-id="0a8ee-118">This value is often called the "Terminal ID" or “TID”.</span></span> <span data-ttu-id="0a8ee-119">โดยทั่วไปคุณจะพบ TID บนสติกเกอร์บนอุปกรณ์การชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="0a8ee-119">The TID can generally be found on a sticker on the payment device.</span></span>  
9. <span data-ttu-id="0a8ee-120">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="0a8ee-120">Click Save.</span></span>


