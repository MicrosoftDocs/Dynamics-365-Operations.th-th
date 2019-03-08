---
title: เพิ่มผลิตภัณฑ์ย่อยโดยใช้น้ำหนักย่อยใบสั่งซื้อ
description: 'กระบวนการนี้นำไปสู่ขั้นตอนสำหรับการใช้น้ำหนักย่อยที่จะเติมบรรทัดรายการข้อมูลใบสั่งซื้ออัตโนมัติสำหรับแต่ละผลิตภัณฑ์ย่อย '
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 446260a09bd5177877637ac8a288ad584dfa2b2b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/29/2019
ms.locfileid: "345501"
---
# <a name="add-variant-products-to-purchase-orders-using-variant-weights"></a><span data-ttu-id="4e567-103">เพิ่มผลิตภัณฑ์ย่อยโดยใช้น้ำหนักย่อยใบสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="4e567-103">Add variant products to purchase orders using variant weights</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4e567-104">กระบวนการนี้นำไปสู่ขั้นตอนสำหรับการใช้น้ำหนักย่อยที่จะเติมบรรทัดรายการข้อมูลใบสั่งซื้ออัตโนมัติสำหรับแต่ละผลิตภัณฑ์ย่อย </span><span class="sxs-lookup"><span data-stu-id="4e567-104">This procedure walks through the steps for using variant weights to auto populate purchase order lines for each variant of a product.</span></span> <span data-ttu-id="4e567-105">เมื่อคุณเลือกปริมาณของผลิตภัณฑ์ที่คุณต้องการซื้อแล้ว รายการใบสั่งซื้อจะถูกสร้างขึ้นสำหรับผลิตภัณฑ์ย่อยทั้งหมดด้วยปริมาณที่แนะนำตามน้ำหนักที่กำหนดค่าไว้ในผลิตภัณฑ์ย่อย </span><span class="sxs-lookup"><span data-stu-id="4e567-105">When you select the quantity of the product you want to purchase, purchase order lines are created for all the variants of the product with suggested quantities based on the weights configured on the product variants.</span></span> <span data-ttu-id="4e567-106">กระบวนการนี้ไม่รวมขั้นตอนในการตั้งค่าคอนฟิกค่าน้ำหนักในมิติของผลิตภัณฑ์และผลิตภัณฑ์ย่อย </span><span class="sxs-lookup"><span data-stu-id="4e567-106">This procedure doesn’t include steps to configure weight values on product dimensions and product variants.</span></span> <span data-ttu-id="4e567-107">กระบวนงานนี้ใช้บริษัท USRT ในข้อมูลสาธิต</span><span class="sxs-lookup"><span data-stu-id="4e567-107">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="4e567-108">ไปที่บัญชีเจ้าหนี้ > ใบสั่งซื้อ > ใบสั่งซื้อทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="4e567-108">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="4e567-109">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="4e567-109">Click New.</span></span>
3. <span data-ttu-id="4e567-110">ในฟิลด์บัญชีผู้จัดจำหน่าย ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="4e567-110">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="4e567-111">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="4e567-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="4e567-112">เปิดปิดการขยายของส่วนทั่วไป</span><span class="sxs-lookup"><span data-stu-id="4e567-112">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="4e567-113">ในฟิลด์ไซต์ ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="4e567-113">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="4e567-114">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="4e567-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="4e567-115">ในฟิลด์คลังสินค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="4e567-115">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="4e567-116">ในรายการนี้ ให้ค้นหาและเลือกเรกคอร์ดที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="4e567-116">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="4e567-117">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="4e567-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="4e567-118">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="4e567-118">Click OK.</span></span>
12. <span data-ttu-id="4e567-119">สลับการขยายของส่วนรายละเอียดรายการ</span><span class="sxs-lookup"><span data-stu-id="4e567-119">Toggle the expansion of the Line details section.</span></span>
13. <span data-ttu-id="4e567-120">คลิกแท็บตัวแปร</span><span class="sxs-lookup"><span data-stu-id="4e567-120">Click the Variants tab.</span></span>
14. <span data-ttu-id="4e567-121">คลิกเพิ่มรายการ</span><span class="sxs-lookup"><span data-stu-id="4e567-121">Click Add line.</span></span>
15. <span data-ttu-id="4e567-122">ในรายการนี้ ให้ทำเครื่องหมายแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="4e567-122">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="4e567-123">ในฟิลด์หมายเลขสินค้า ให้พิมพ์ '0140'</span><span class="sxs-lookup"><span data-stu-id="4e567-123">In the Item number field, type '0140'.</span></span>
17. <span data-ttu-id="4e567-124">กำหนดปริมาณเป็น '1000'</span><span class="sxs-lookup"><span data-stu-id="4e567-124">Set Quantity to '1000'.</span></span>
18. <span data-ttu-id="4e567-125">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="4e567-125">Click Save.</span></span>

