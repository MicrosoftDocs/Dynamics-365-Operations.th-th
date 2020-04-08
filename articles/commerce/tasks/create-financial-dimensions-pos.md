---
title: " สร้างค่ามิติทางการเงินสำหรับเครื่องบันทึกเงินสด POS และตั้งค่าคอนฟิกค่ามิติบนเครื่องบันทึกเงินสด"
description: 'กระบวนการนี้นำไปสู่การสร้างมิติทางการเงินสำหรับการลงทะเบียนการขายหน้าร้าน (POS) และแสดงวิธีการตั้งค่าคอนฟิกค่ามิติทางการเงินบนเครื่องบันทึกเงินสด '
author: jashanno
manager: AnnBe
ms.date: 11/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7be50eba098b7b28594c8e18c721579f4bb2e879
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141002"
---
# <a name="create-financial-dimensions-for-pos-registers-and-configure-dimension-values-on-registers"></a><span data-ttu-id="fc459-103"> สร้างค่ามิติทางการเงินสำหรับเครื่องบันทึกเงินสด POS และตั้งค่าคอนฟิกค่ามิติบนเครื่องบันทึกเงินสด</span><span class="sxs-lookup"><span data-stu-id="fc459-103">Create financial dimensions for POS registers and configure dimension values on registers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fc459-104">กระบวนการนี้นำไปสู่การสร้างมิติทางการเงินสำหรับการลงทะเบียนการขายหน้าร้าน (POS) และแสดงวิธีการตั้งค่าคอนฟิกค่ามิติทางการเงินบนเครื่องบันทึกเงินสด </span><span class="sxs-lookup"><span data-stu-id="fc459-104">This procedure walks through creating financial dimensions for point of sale (POS) registers, and demonstrates how to configure financial dimension values on registers.</span></span> <span data-ttu-id="fc459-105">กระบวนงานนี้ไม่รวมขั้นตอนที่เกี่ยวข้องอื่นๆ เช่น การสร้างชุดมิติและโครงสร้างทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="fc459-105">This procedure doesn't include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="fc459-106">งานเหล่านั้นจะถูกพบได้ในหัวข้ออื่นๆ</span><span class="sxs-lookup"><span data-stu-id="fc459-106">Those tasks can be found in other topics.</span></span> <span data-ttu-id="fc459-107">บันทึกนี้ใช้บริษัทสาธิต USRT</span><span class="sxs-lookup"><span data-stu-id="fc459-107">This recording uses USRT demo company.</span></span>

1. <span data-ttu-id="fc459-108">ไปที่บัญชีแยกประเภททั่วไป > ผังบัญชี > มิติ > มิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="fc459-108">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="fc459-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="fc459-109">Click New.</span></span>
3. <span data-ttu-id="fc459-110">ในฟิลด์ ใช้ค่าจาก เลือกตัวเลือก</span><span class="sxs-lookup"><span data-stu-id="fc459-110">In the Use values from field, select an option.</span></span>
4. <span data-ttu-id="fc459-111">ในฟิลด์ชื่อมิติ ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="fc459-111">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="fc459-112">คลิกเรียกใช้</span><span class="sxs-lookup"><span data-stu-id="fc459-112">Click Activate.</span></span>
6. <span data-ttu-id="fc459-113">คลิก ปิด</span><span class="sxs-lookup"><span data-stu-id="fc459-113">Click Close.</span></span>
7. <span data-ttu-id="fc459-114">คลิกเรียกใช้</span><span class="sxs-lookup"><span data-stu-id="fc459-114">Click Activate.</span></span>
8. <span data-ttu-id="fc459-115">คลิกค่ามิติ</span><span class="sxs-lookup"><span data-stu-id="fc459-115">Click Dimension values.</span></span>
9. <span data-ttu-id="fc459-116">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="fc459-116">Close the page.</span></span>
10. <span data-ttu-id="fc459-117">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="fc459-117">Click Save.</span></span>
11. <span data-ttu-id="fc459-118">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="fc459-118">Close the page.</span></span>
12. <span data-ttu-id="fc459-119">ไปยัง Retail และ Commerce > การตั้งค่าช่องทาง > การตั้งค่า POS > การลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="fc459-119">Go to Retail and Commerce > Channel setup > POS setup > Registers.</span></span>
13. <span data-ttu-id="fc459-120">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="fc459-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="fc459-121">สลับการขยายของส่วนมิติการเงิน</span><span class="sxs-lookup"><span data-stu-id="fc459-121">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="fc459-122">คลิกแก้ไข</span><span class="sxs-lookup"><span data-stu-id="fc459-122">Click Edit.</span></span>
16. <span data-ttu-id="fc459-123">ในฟิลด์ เทอร์มินัล คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="fc459-123">In the Terminal field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="fc459-124">ในรายการ ให้ค้นหาและเลือกค่ามิติสำหรับการลงทะเบียนที่กำลังถูกอัพเดต</span><span class="sxs-lookup"><span data-stu-id="fc459-124">In the list, find and select the dimension value for the register being updated.</span></span>
18. <span data-ttu-id="fc459-125">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="fc459-125">Click Save.</span></span>

