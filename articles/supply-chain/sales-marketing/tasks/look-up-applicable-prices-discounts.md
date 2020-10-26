---
title: ค้นหาราคาและส่วนลดที่เกี่ยวข้อง
description: 'ขั้นตอนนี้แสดงวิธีการค้นหาราคาและ/หรือส่วนลดสำหรับผลิตภัณฑ์ที่มีผลบังคับใช้สำหรับลูกค้าเฉพาะรายโดยไม่มีการสร้างใบสั่งขาย '
author: omulvad
manager: tfehr
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2cfdbda55c2f83ee2b470cab8a5e4f9ce728b852
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982124"
---
# <a name="look-up-applicable-prices-and-discounts"></a><span data-ttu-id="8fa01-103">ค้นหาราคาและส่วนลดที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="8fa01-103">Look up applicable prices and discounts</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8fa01-104">ขั้นตอนนี้แสดงวิธีการค้นหาราคาและ/หรือส่วนลดสำหรับผลิตภัณฑ์ที่มีผลบังคับใช้สำหรับลูกค้าเฉพาะรายโดยไม่มีการสร้างใบสั่งขาย </span><span class="sxs-lookup"><span data-stu-id="8fa01-104">This procedure shows how to find the price and/or discount for a product which is currently valid for a specific customer, without creating a sales order.</span></span> <span data-ttu-id="8fa01-105">กระบวนการดังดล่าวนำไปสู่ตัวอย่างเฉพาะ และคุณต้องทำตามตัวอย่างโดยใช้ข้อมูลสาธิตบริษัท USMF เพื่อเลือกค่าจำเป็น</span><span class="sxs-lookup"><span data-stu-id="8fa01-105">The procedure walks through a specific example, and you need follow the example using the USMF demo company in order to select the necessary values.</span></span>


## <a name="find-the-applicable-price"></a><span data-ttu-id="8fa01-106">ค้นหาราคาที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="8fa01-106">Find the applicable price</span></span>
1. <span data-ttu-id="8fa01-107">ไปยัง การขายและการตลาด > ราคาและส่วนลด > ค้าหาราคา</span><span class="sxs-lookup"><span data-stu-id="8fa01-107">Go to Sales and marketing > Prices and discounts > Find prices.</span></span>
2. <span data-ttu-id="8fa01-108">ในฟิลด์บัญชีลูกค้า ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="8fa01-108">In the Customer account field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="8fa01-109">ในรายการนี้ ให้ค้นหาและเลือกลูกค้า US-001</span><span class="sxs-lookup"><span data-stu-id="8fa01-109">In the list, find and select customer US-001.</span></span>
4. <span data-ttu-id="8fa01-110">ในรายการนี้ ให้คลิกลิงค์ในแถวที่เลือก</span><span class="sxs-lookup"><span data-stu-id="8fa01-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="8fa01-111">ในฟิลด์ หมายเลขสินค้า ให้พิมพ์ 'T0004'</span><span class="sxs-lookup"><span data-stu-id="8fa01-111">In the Item number field, type 'T0004'.</span></span>
    * <span data-ttu-id="8fa01-112">ตามค่าเริ่มต้น ฟิลด์ปริมาณถูกตั้งค่าเป็น 1</span><span class="sxs-lookup"><span data-stu-id="8fa01-112">By default, the Quantity field is set to 1.</span></span> <span data-ttu-id="8fa01-113">อย่างไรก็ตาม ถ้าคุณทราบขนาดของใบสั่งที่ลูกค้าต้องการสำหรับผลิตภัณฑ์ในคำถามแล้ว ให้ป้อนค่านี้แทน</span><span class="sxs-lookup"><span data-stu-id="8fa01-113">However, if you know the size of the order that the customer intends to place for the product in question, then enter this value instead.</span></span> <span data-ttu-id="8fa01-114">ข้อมูลนี้จะเกี่ยวข้องถ้าข้อตกลงทางการค้ากับลูกค้าที่มีการแบ่งปริมาณ นั่นคือ ราคาของผลิตภัณฑ์ขึ้นอยู่กับปริมาณต่ำสุดที่ซื้อ</span><span class="sxs-lookup"><span data-stu-id="8fa01-114">This information is relevant if the trade agreements with the customer have quantity breaks, that is, the product's price depends on the minimum quantity purchased.</span></span>  
6. <span data-ttu-id="8fa01-115">ในฟิลด์วัน ป้อนวันที่ที่ลูกค้าคาดว่าจะสั่งซื้อ</span><span class="sxs-lookup"><span data-stu-id="8fa01-115">In the Date field, enter a date for when the customer expects to place an order.</span></span> 
    * <span data-ttu-id="8fa01-116">วันอาจเป็นวันที่ของวันนี้หรือวันในอนาคต</span><span class="sxs-lookup"><span data-stu-id="8fa01-116">The date can be today's date or any date in the future.</span></span>  
    * <span data-ttu-id="8fa01-117">ขณะนี้ระบบส่งกลับค่าราคาที่ถูกต้องสำหรับผลิตภัณฑ์ที่เลือกเมื่อถูกซื้อโดยลูกค้าที่เลือกในวันที่เลือกและมีการระบุปริมาณ </span><span class="sxs-lookup"><span data-stu-id="8fa01-117">The system now returns the price that is valid for the selected product when bought by the selected customer on the selected date with a specified quantity.</span></span> <span data-ttu-id="8fa01-118">ในตัวอย่างนี้ ถ้าลูกค้า US-001 ซื้อ 1 หน่วยของผลิตภัณฑ์ T0004 วันนี้ พวกเขาจะสามารถคิดค่าธรรมเนียม CAD 350 ต่อหน่วย</span><span class="sxs-lookup"><span data-stu-id="8fa01-118">In this example, if the customer US-001 bought 1 unit of product T0004 today, they would be charged 350 CAD a unit.</span></span> <span data-ttu-id="8fa01-119">ราคานี้มาจากข้อตกลงทางการค้าที่มีอยู่และใช้งานอยู่กับลูกค้า </span><span class="sxs-lookup"><span data-stu-id="8fa01-119">This price comes from an existing and active trade agreement with the customer.</span></span>      <span data-ttu-id="8fa01-120">ฟิลด์อื่นๆบนหน้าแสดงรายละเอียดเพิ่มเติมเกี่ยวกับราคาผลิตภัณฑ์และต้นทุนผลิตภัณฑ์ (หากตั้งค่าไว้ในผลิตภัณฑ์หลัก) และกำไรที่คำนวณได้</span><span class="sxs-lookup"><span data-stu-id="8fa01-120">Other fields on the page provide more details about the product price and product cost (if set up on the product master), and calculated profitability.</span></span>  
    * <span data-ttu-id="8fa01-121">ถ้ารายการที่เกี่ยวข้องกับผลิตภัณฑ์ย่อยถูกเลือก หมายความว่ามีข้อตกลงทางการค้าเพิ่มเติมสำหรับตัวแปรของผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="8fa01-121">If the Show related product variants option is selected, it means that there are additional trade agreements for product's variants.</span></span>  
7. <span data-ttu-id="8fa01-122">คลิกกล่องกาเครื่องหมายแสดงรายการตัวแปรผลิตภัณฑ์ที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="8fa01-122">Click the Show related product variants checkbox.</span></span>
    * <span data-ttu-id="8fa01-123">รายการของผลิตภัณฑ์ย่อยจะแสดงขึ้นร่วมกับข้อมูลเกี่ยวกับมิติของสินค้า</span><span class="sxs-lookup"><span data-stu-id="8fa01-123">A list of the product variants is shown, with information about their dimensions.</span></span>  
8. <span data-ttu-id="8fa01-124">ในรายการ ทำเครื่องหมายรายการที่แสดงสีขาว</span><span class="sxs-lookup"><span data-stu-id="8fa01-124">In the list, mark the line representing color White.</span></span>
    * <span data-ttu-id="8fa01-125">โปรดสังเกต ตอนนี้ราคาผลิตภัณฑ์จะแตกต่างจากข้อมูลที่แสดงไว้ก่อนหน้านี้เมื่อไม่มีการระบุสำหรับแต่ละมิติ</span><span class="sxs-lookup"><span data-stu-id="8fa01-125">Notice, that the product price is now different from the one displayed previously when it was not specified per dimension.</span></span>  
9. <span data-ttu-id="8fa01-126">คลิกดูราคาขาย</span><span class="sxs-lookup"><span data-stu-id="8fa01-126">Click View sales prices.</span></span>
    * <span data-ttu-id="8fa01-127">หน้าราคา (ขาย) แสดงข้อตกลงทางการค้าทั้งหมดที่เกี่ยวข้องกับผลิตภัณฑ์ รวมถึงของผลิตภัณฑ์ย่อย</span><span class="sxs-lookup"><span data-stu-id="8fa01-127">The Price (sales) page displays all the trade agreements applicable to the product, including its variants.</span></span>  
10. <span data-ttu-id="8fa01-128">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="8fa01-128">Close the page.</span></span>

## <a name="find-the-applicable-discount"></a><span data-ttu-id="8fa01-129">ค้นหาส่วนลดที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="8fa01-129">Find the applicable discount</span></span>
<span data-ttu-id="8fa01-130">ตรวจสอบว่า ฟิลด์บัญชีลูกค้าประกอบด้วยหมายเลขลูกค้า US-001</span><span class="sxs-lookup"><span data-stu-id="8fa01-130">Make sure the Customer account field contains customer number US-001</span></span>   
1. <span data-ttu-id="8fa01-131">ในฟิลด์ หมายเลขสินค้า ให้พิมพ์ 'T0012'</span><span class="sxs-lookup"><span data-stu-id="8fa01-131">In the Item number field, type 'T0012'.</span></span>
    * <span data-ttu-id="8fa01-132">ตรวจสอบให้แน่ใจว่า ฟิลด์ปริมาณถูกตั้งค่าเป็น 1</span><span class="sxs-lookup"><span data-stu-id="8fa01-132">Make sure the Quantity field is set to 1.</span></span>  
    * <span data-ttu-id="8fa01-133">รายละเอียดราคาต่อไปนี้แสดงสำหรับผลิตภัณฑ์ T0012 มาจากข้อตกลงทางการค้าหนึ่งข้อตกลงหรือหลายข้อตกลง: ราคาต่อหน่วยคือ CAD 1000 และเปอร์เซ็นต์ส่วนลดเป็น 5</span><span class="sxs-lookup"><span data-stu-id="8fa01-133">The following pricing details shown for product T0012 come from one or more trade agreements: The unit price is 1,000 CAD and the discount percentage is 5.</span></span>  
2. <span data-ttu-id="8fa01-134">กำหนดปริมาณเป็น '20'</span><span class="sxs-lookup"><span data-stu-id="8fa01-134">Set Quantity to '20'.</span></span>
    * <span data-ttu-id="8fa01-135">ปริมาณใบสั่งที่เพิ่มขึ้นทำให้ส่วนลดต่อรายการสินค้าที่จะนำเสนอให้แก่ลูกค้าจะเปลี่ยนจาก 5 ถึง 7 เปอร์เซ็นต์</span><span class="sxs-lookup"><span data-stu-id="8fa01-135">The increased order quantity causes the line discount that will be offered to the customer to change from 5 to 7 percent.</span></span>  
    * <span data-ttu-id="8fa01-136">ระบบจะคำนวณยอดเงินสุทธิตามเงื่อนไขราคาต่อหน่วย ส่วนลดและปริมาณรวม</span><span class="sxs-lookup"><span data-stu-id="8fa01-136">The Net amount is calculated based on the unit price, discount and the total quantity.</span></span>  
3. <span data-ttu-id="8fa01-137">คลิกดูส่วนลดต่อรายการสินค้า</span><span class="sxs-lookup"><span data-stu-id="8fa01-137">Click View line discount.</span></span>
    * <span data-ttu-id="8fa01-138">มีสองรายการข้อตกลงส่วนลดสำหรับผลิตภัณฑ์ T0012 ระบุส่วนลด 5 เปอร์เซ็นต์สำหรับปริมาณรายการใบสั่งจาก 1 ถึง 10 และ ส่วนลด 7 เปอร์เซ็นต์สำหรับปริมาณใบสั่งสูงกว่า 10</span><span class="sxs-lookup"><span data-stu-id="8fa01-138">There are two line discount agreements for product T0012, specifying a 5 percent discount for an order line quantity from 1 to 10, and 7 percent discount for order quantities above 10.</span></span> <span data-ttu-id="8fa01-139">โปรดทราบว่าส่วนลดที่ใช้กับกลุ่มของผลิตภัณฑ์ ในตัวอย่างนี้ กลุ่มรหัส 01 ผลิตภัณฑ์ใด T0012 เป็นสมาชิก</span><span class="sxs-lookup"><span data-stu-id="8fa01-139">Note that the discounts are applied to a group of products, in this example, Group code 01, of which product T0012 is a member.</span></span>  
4. <span data-ttu-id="8fa01-140">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="8fa01-140">Close the page.</span></span>

