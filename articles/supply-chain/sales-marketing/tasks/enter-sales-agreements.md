---
title: ป้อนข้อตกลงการขาย
description: หัวข้อนี้อธิบายวิธีการสร้างข้อตกลงการขายที่ยืนยันหนึ่งในลูกค้าของคุณให้ซื้อผลิตภัณฑ์เป็นจำนวนที่ตกลงกันตามช่วงเวลาในการแลกเปลี่ยนสำหรับส่วนลดพิเศษ
author: omulvad
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesAgreementListPage, SalesAgreementCreate, SalesAgreement, InventItemIdLookupSimple, AgreementConfirmRunForm, SrsReportViewerForm, SalesAgreementCustomerReferencesPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4828b6f2f66c7ca33db0a3401d0f2fae78e39e65
ms.sourcegitcommit: 54da65a7da0efd4f0d9760c5b14ff785b28751c4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/22/2020
ms.locfileid: "3830172"
---
# <a name="enter-sales-agreements"></a><span data-ttu-id="ee3e5-103">ป้อนข้อตกลงการขาย</span><span class="sxs-lookup"><span data-stu-id="ee3e5-103">Enter sales agreements</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ee3e5-104">หัวข้อนี้อธิบายวิธีการสร้างข้อตกลงการขายที่ยืนยันหนึ่งในลูกค้าของคุณให้ซื้อผลิตภัณฑ์เป็นจำนวนที่ตกลงกันตามช่วงเวลาในการแลกเปลี่ยนสำหรับส่วนลดพิเศษ</span><span class="sxs-lookup"><span data-stu-id="ee3e5-104">This topic explains how to create a sales agreement that commits one of your customers to buy a product for an agreed amount over time in exchange for special discounts.</span></span> <span data-ttu-id="ee3e5-105">คุณสามารถเรียกใช้ขั้นตอนนี้ ในบริษัทข้อมูลสาธิต USMF หรือข้อมูลของคุณเอง</span><span class="sxs-lookup"><span data-stu-id="ee3e5-105">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-sales-agreement-header"></a><span data-ttu-id="ee3e5-106">ตั้งค่าส่วนหัวข้อตกลงการขาย</span><span class="sxs-lookup"><span data-stu-id="ee3e5-106">Set up sales agreement header</span></span>
1. <span data-ttu-id="ee3e5-107">ในบานหน้าต่างนำทาง ให้ไปที่ **โมดูล > ข้อตกลงการขายและการตลาด > ข้อตกลงการขาย > ข้อตกลงการขาย**</span><span class="sxs-lookup"><span data-stu-id="ee3e5-107">In the navigation pane, go to **Modules > Sales and marketing > Sales agreements > Sales agreements**.</span></span>
2. <span data-ttu-id="ee3e5-108">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="ee3e5-108">Select **New**.</span></span>
3. <span data-ttu-id="ee3e5-109">ในฟิลด์ **บัญชีลูกค้า** ให้เลือกเรกคอร์ดที่ต้องการจากเมนูแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="ee3e5-109">In the **Customer account** field, select the desired record from the drop-down menu.</span></span>
4. <span data-ttu-id="ee3e5-110">ในฟิลด์ **การจัดประเภทข้อตกลงการขาย** ให้เลือกเรกคอร์ดที่ต้องการจากเมนูแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="ee3e5-110">In the **Sales agreement classification** field, select the desired record from the drop-down menu.</span></span>
5. <span data-ttu-id="ee3e5-111">ขยายส่วน **ทั่วไป**</span><span class="sxs-lookup"><span data-stu-id="ee3e5-111">Expand the **General** section.</span></span>
6. <span data-ttu-id="ee3e5-112">ในฟิลด์ **ข้อผูกมัดเริ่มต้น** เลือก **ข้อผูกมัดมูลค่าผลิตภัณฑ์'**</span><span class="sxs-lookup"><span data-stu-id="ee3e5-112">In the **Default commitment** field, select **Product value commitment**.</span></span> <span data-ttu-id="ee3e5-113">ประเภทข้อผูกมัดไม่บังคับใช้หลักเกณฑ์ที่คุณต้องมอบหมายไปยังข้อตกลงเพื่อกำหนดว่าจะครบถ้วนตามที่ทำสัญญา</span><span class="sxs-lookup"><span data-stu-id="ee3e5-113">A commitment type is a mandatory criterion that you must assign to the agreement to define how the agreement contract will be fulfilled.</span></span> <span data-ttu-id="ee3e5-114">สี่ประเภทที่กำหนดไว้ล่วงหน้าช่วยให้คุณตั้งค่าเป้าหมายข้อผูกมัดของลูกค้า แสดงเป็นปริมาณหรือค่า</span><span class="sxs-lookup"><span data-stu-id="ee3e5-114">The four predefined types let you set up the customer's commitment target, expressed as a quantity or a value.</span></span> <span data-ttu-id="ee3e5-115">ชนิดข้อผูกมัดของปริมาณสามารถใช้ได้เฉพาะกับผลิตภัณฑ์ที่ระบุ แต่ชนิดตามมูลค่าจะสามารถใช้ได้กับการขายของผลิตภัณฑ์ทั้งเฉพาะและไม่ใช่เฉพาะเจาะจง</span><span class="sxs-lookup"><span data-stu-id="ee3e5-115">The quantity commitment type can only be applied to a specific product, but the value-based types are applicable to sales of both specific and non-specific products.</span></span>  
7. <span data-ttu-id="ee3e5-116">ในฟิลด์ **วันหมดอายุ** ตั้งค่าวันที่เป็นวันที่ในอนาคต เมื่อคุณต้องการให้ข้อตกลงหมดอายุ</span><span class="sxs-lookup"><span data-stu-id="ee3e5-116">In the **Expiration date** field, set the date to a future date when you want the agreement to expire.</span></span>
8. <span data-ttu-id="ee3e5-117">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="ee3e5-117">Select **OK**.</span></span>

## <a name="set-up-product-value-commitment-lines"></a><span data-ttu-id="ee3e5-118">ตั้งค่ารายการข้อผูกมัดเกี่ยวกับมูลค่าผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="ee3e5-118">Set up product value commitment lines</span></span>
1. <span data-ttu-id="ee3e5-119">เลือก **เพิ่มรายการ**</span><span class="sxs-lookup"><span data-stu-id="ee3e5-119">Select **Add line**.</span></span>
2. <span data-ttu-id="ee3e5-120">ในฟิลด์ **หมายเลขสินค้า** ให้เลือกเรกคอร์ดที่ต้องการจากเมนูแบบหล่นลง</span><span class="sxs-lookup"><span data-stu-id="ee3e5-120">In the **Item number** field, select the desired record from the drop-down menu.</span></span> <span data-ttu-id="ee3e5-121">ชนิดของข้อผูกมัดที่คุณเลือกสำหรับข้อตกลงมีผลต่อชนิดของข้อมูลที่คุณสามารถป้อนสำหรับรายการข้อตกลง </span><span class="sxs-lookup"><span data-stu-id="ee3e5-121">The type of commitment that you have chosen for the agreement affects the kind of information you can enter for the agreement lines.</span></span> <span data-ttu-id="ee3e5-122">ตัวอย่างเช่น สำหรับข้อตกลงตามค่าที่คุณต้องระบุยอดรวมสุทธิ (ในสกุลเงินที่ตกลงกัน) สำหรับลูกค้าที่ตกลงจะซื้อสินค้าจากคุณ</span><span class="sxs-lookup"><span data-stu-id="ee3e5-122">For example, for a value-based agreement you must specify the total net amount (in the agreed currency) for which the customer commits to buys goods from you.</span></span> <span data-ttu-id="ee3e5-123">ในตัวอย่างนี้ ฟิลด์ **ปริมาณ** และ **หน่วย** ในรายการ ไม่พร้อมใช้งานเนื่องจากคุณกำลังสร้างข้อตกลงสำหรับลูกค้าเพื่อจะซื้อผลิตภัณฑ์ตามค่าที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="ee3e5-123">In this example the **Quantity** and **Unit** fields on the line are unavailable because you're creating an agreement for the customer to buy a specific value of a product.</span></span>   
3. <span data-ttu-id="ee3e5-124">ในฟิลด์ **ยอดเงินสุทธิ** ป้อนยอดเงินที่ลูกค้าได้ตกลงที่จะซื้อ</span><span class="sxs-lookup"><span data-stu-id="ee3e5-124">In the **Net amount** field, enter the monetary amount that the customer has committed to buying.</span></span>
4. <span data-ttu-id="ee3e5-125">ในฟิลด์ **เปอร์เซ็นต์ส่วนลด** ป้อนค่าเปอร์เซ็นต์ที่จะใช้กับรายการใบสั่งขายของลูกค้าที่เชื่อมโยงกับข้อตกลงนี้</span><span class="sxs-lookup"><span data-stu-id="ee3e5-125">In the **Discount percent** field, enter a percentage value that will apply to the customer's sales order lines that are linked to this agreement.</span></span>
5. <span data-ttu-id="ee3e5-126">ขยายส่วน **รายละเอียดรายการ**</span><span class="sxs-lookup"><span data-stu-id="ee3e5-126">Expand the **Line details** section.</span></span>
6. <span data-ttu-id="ee3e5-127">เลือก **ใช่** ในฟิลด์ **บังคับใช้ค่าสูงสุด**</span><span class="sxs-lookup"><span data-stu-id="ee3e5-127">Select **Yes** in the **Max is enforced** field.</span></span>
    - <span data-ttu-id="ee3e5-128">การเลือก **บังคับใช้ค่าสูงสุด** หมายความว่า จำนวนรวมของรายการใบสั่งขายทั้งหมดที่ใช้ราคาพิเศษของข้อผูกมัด ส่วนลด และ/หรือเงื่อนไขการชำระเงิน ต้องไม่เกินจำนวนที่ระบุในข้อผูกมัด</span><span class="sxs-lookup"><span data-stu-id="ee3e5-128">Selecting **Max is enforced** means that the total amount of all the sales order lines that use the commitment's special prices, discounts and/or payment terms must not exceed the amount specified on the commitment.</span></span>  
    - <span data-ttu-id="ee3e5-129">จำนวนเงินนำออกใช้ต่ำสุดและสูงสุดระบุช่วงของมูลค่าที่ต้องขายในใบสั่งขายแต่ละรายการที่ใช้ข้อตกลงที่เลือก</span><span class="sxs-lookup"><span data-stu-id="ee3e5-129">The minimum and maximum release amounts specify a range of values that must be sold on each sales order that uses the selected agreement.</span></span>   
7. <span data-ttu-id="ee3e5-130">ขยายส่วน **ส่วนหัวของข้อตกลงการขาย**</span><span class="sxs-lookup"><span data-stu-id="ee3e5-130">Expand the **Sales agreement header** section.</span></span> <span data-ttu-id="ee3e5-131">ถ้าไม่มีการตั้งค่าสถานะของข้อตกลงเป็น **มีผลบังคับใช้** ใบสั่งขายจะไม่สามารถเชื่อมโยงกับข้อตกลง และดังนั้นจึงไม่สามารถจัดสรรเป็นส่วนเติมเต็มข้อตกลงนั้นได้</span><span class="sxs-lookup"><span data-stu-id="ee3e5-131">Unless the status of the agreement is set to **Effective**, sales orders cannot be associated with the agreement and can therefore not contribute to the fulfilment of that agreement.</span></span> <span data-ttu-id="ee3e5-132">คุณสามารถเปลี่ยนสถานะด้วยตนเองในขั้นตอนนี้</span><span class="sxs-lookup"><span data-stu-id="ee3e5-132">You can change the status manually at this stage.</span></span> <span data-ttu-id="ee3e5-133">อย่างไรก็ตาม สถานะจะถูกเปลี่ยนตามปกติเมื่อคุณยืนยันข้อตกลงสำหรับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="ee3e5-133">However, the status would normally be changed when you confirm the agreement for the customer.</span></span>  
8. <span data-ttu-id="ee3e5-134">บนหน้าต่างการดำเนินการ เลือก **ข้อตกลงการขาย**</span><span class="sxs-lookup"><span data-stu-id="ee3e5-134">On the Action Pane, select **Sales agreement**.</span></span>
9. <span data-ttu-id="ee3e5-135">เลือก **การยืนยัน**</span><span class="sxs-lookup"><span data-stu-id="ee3e5-135">Select **Confirmation**.</span></span> <span data-ttu-id="ee3e5-136">ตรวจสอบให้แน่ใจว่าตัวเลือก **ทำเครื่องหมายข้อตกลงเป็นมีผลบังคับใช้** ถูกตั้งค่าเป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="ee3e5-136">Make sure that the **Mark agreement as effective** option is set to **Yes**.</span></span>  
10. <span data-ttu-id="ee3e5-137">เลือก **ใช่** ในฟิลด์ **พิมพ์รายงาน**</span><span class="sxs-lookup"><span data-stu-id="ee3e5-137">Select **Yes** in the **Print report** field.</span></span>
11. <span data-ttu-id="ee3e5-138">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="ee3e5-138">Select **OK**.</span></span>
12. <span data-ttu-id="ee3e5-139">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="ee3e5-139">Close the page.</span></span> <span data-ttu-id="ee3e5-140">ขณะนี้ข้อตกลงมีผลบังคับใช้</span><span class="sxs-lookup"><span data-stu-id="ee3e5-140">The agreement is now effective.</span></span> <span data-ttu-id="ee3e5-141">คุณสามารถเริ่มต้นการเชื่อมโยงใบสั่งของลูกค้ากับข้อตกลงเพื่อออฟเซ็ตกับเป้าหมายผูกมัด</span><span class="sxs-lookup"><span data-stu-id="ee3e5-141">You can start linking the customer's orders to the agreement to offset against the committed target.</span></span>  

