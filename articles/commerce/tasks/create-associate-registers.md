---
title: " สร้างและเชื่อมโยงการลงทะเบียน"
description: 'กระบวนงานนี้อธิบายวิธีการสร้างเครื่องบันทึกเงินสดการขายหน้าร้าน (POS) '
author: rubencdelgado
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailTerminalTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0ac75d390b8bbb94c6e039b374b51462d348e355
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057195"
---
# <a name="create-and-associate-registers"></a><span data-ttu-id="79f9e-103"> สร้างและเชื่อมโยงการลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="79f9e-103">Create and associate registers</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="79f9e-104">กระบวนงานนี้อธิบายวิธีการสร้างเครื่องบันทึกเงินสดการขายหน้าร้าน (POS) </span><span class="sxs-lookup"><span data-stu-id="79f9e-104">This procedure demonstrates how to create a point of sale (POS) register.</span></span> <span data-ttu-id="79f9e-105">กระบวนงานนี้ใช้ข้อมูลบริษัทสาธิต USRT</span><span class="sxs-lookup"><span data-stu-id="79f9e-105">This procedure uses the demo data company USRT.</span></span>

1. <span data-ttu-id="79f9e-106">ไปยัง Retail และ Commerce > การตั้งค่าช่องทาง > การตั้งค่า POS > การลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="79f9e-106">Go to Retail and Commerce > Channel setup > POS setup > Registers.</span></span>
2. <span data-ttu-id="79f9e-107">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="79f9e-107">Click New.</span></span>
3. <span data-ttu-id="79f9e-108">ในฟิลด์หมายเลขเครื่องบันทึกเงินสด ให้พิมพ์รหัสสำหรับเครื่องบันทึกเงินสดใหม่</span><span class="sxs-lookup"><span data-stu-id="79f9e-108">In the Register number field, type an ID for the new register.</span></span>
    * <span data-ttu-id="79f9e-109">โดยทั่วไปรหัสเครื่องบันทึกเงินสดจะประกอบด้วยรหัสที่ช่วยในการแม็ปเครื่องบันทึกเงินสดให้กับร้านค้าที่เป็นเจ้าของ และสถานที่ภายในร้านค้า</span><span class="sxs-lookup"><span data-stu-id="79f9e-109">The register ID typically includes codes that help map the register to the store to which it belongs, and the location within the store.</span></span>  
4. <span data-ttu-id="79f9e-110">ในฟิลด์ชื่อ ให้พิมพ์ชื่อที่เป็นคำอธิบายสำหรับเครื่องบันทึกเงินสด</span><span class="sxs-lookup"><span data-stu-id="79f9e-110">In the Name field, type a descriptive name for the register..</span></span>
5. <span data-ttu-id="79f9e-111">ในฟิลด์หมายเลขร้านค้า ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="79f9e-111">In the Store number field, enter or select a value.</span></span>
6. <span data-ttu-id="79f9e-112">ในฟิลด์โพรไฟล์ฮาร์ดแวร์ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="79f9e-112">In the Hardware profile field, enter or select a value.</span></span>
    * <span data-ttu-id="79f9e-113">โพรไฟล์ฮาร์ดแวร์จะใช้เพื่อระบุอุปกรณ์ต่อพ่วงที่จะเชื่อมต่อกับเครื่องบันทึกเงินสด เช่น ลิ้นชักเงินสด และเครื่องพิมพ์ใบเสร็จ</span><span class="sxs-lookup"><span data-stu-id="79f9e-113">Hardware profiles are used to specify the peripherals that will be connected to the register, such as cash drawer and receipt printer.</span></span>  
7. <span data-ttu-id="79f9e-114">ในฟิลด์โพรไฟล์ภาพ ให้ป้อนหรือเลือกค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="79f9e-114">In the Visual profile field, enter or select a value.</span></span>
    * <span data-ttu-id="79f9e-115">โพรไฟล์ภาพจะใช้เพื่อระบุรูปภาพที่ใช้ในพื้นหลัง POS และหน้าล็อกอิน รวมทั้งชุดรูปแบบสำหรับ POS</span><span class="sxs-lookup"><span data-stu-id="79f9e-115">Visual profiles are used to specify the images used in the POS background and login page as well as themes for the POS.</span></span>  
8. <span data-ttu-id="79f9e-116">ในฟิลด์หมายเลขเครื่องบันทึกเงินสด EFT POS ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="79f9e-116">In the EFT POS register number field, type a value.</span></span>
    * <span data-ttu-id="79f9e-117">หมายเลขเครื่องบันทึกเงินสด EFT POS จะใช้เพื่อแจ้งตัวประมวลผลการชำระเงินว่าเทอร์มินัลการชำระเงินใดจะส่งคำขอตรวจสอบ </span><span class="sxs-lookup"><span data-stu-id="79f9e-117">The EFT POS register number is used to inform the payment processor which payment terminal is sending authorization requests.</span></span> <span data-ttu-id="79f9e-118">ค่านี้มักเรียกว่า "รหัสเทอร์มินัล" หรือ "TID" </span><span class="sxs-lookup"><span data-stu-id="79f9e-118">This value is often called the "Terminal ID" or “TID”.</span></span> <span data-ttu-id="79f9e-119">โดยทั่วไปคุณจะพบ TID บนสติกเกอร์บนอุปกรณ์การชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="79f9e-119">The TID can generally be found on a sticker on the payment device.</span></span>  
9. <span data-ttu-id="79f9e-120">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="79f9e-120">Click Save.</span></span>

