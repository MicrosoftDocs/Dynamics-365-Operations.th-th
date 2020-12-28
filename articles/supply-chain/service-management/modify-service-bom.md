---
title: การแก้ไข BOM การบริการ
description: แก้ไข BOM การบริการ
author: ShylaThompson
manager: tfehr
ms.date: 05/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 962203726cc47e1c9642c53d671d4b63094f2b2c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 10/13/2020
ms.locfileid: "4438632"
---
# <a name="modify-a-service-bom"></a><span data-ttu-id="cb8b4-103">การแก้ไข BOM การบริการ</span><span class="sxs-lookup"><span data-stu-id="cb8b4-103">Modify a Service BOM</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="cb8b4-104">คุณสามารถบันทึกประวัติขององค์ประกอบใน BOM การบริการ </span><span class="sxs-lookup"><span data-stu-id="cb8b4-104">You can record the history of an element in a service BOM.</span></span> <span data-ttu-id="cb8b4-105">ทุกครั้งที่คุณอัพเดตรายการ BOM รายการประวัติจะถูกสร้างขึ้นในบานหน้าต่าง **ประวัติ**</span><span class="sxs-lookup"><span data-stu-id="cb8b4-105">Every time that you update a BOM line, a history line is created in the **History** pane.</span></span> <span data-ttu-id="cb8b4-106">รายการประวัติจะแสดงสถานะปัจจุบันของบรรทัด BOM</span><span class="sxs-lookup"><span data-stu-id="cb8b4-106">The history line shows the current state of the BOM line.</span></span>

## <a name="update-a-service-bom-element"></a><span data-ttu-id="cb8b4-107">อัพเดตองค์ประกอบของ BOM การบริการ</span><span class="sxs-lookup"><span data-stu-id="cb8b4-107">Update a service BOM element</span></span>

1.  <span data-ttu-id="cb8b4-108">คลิก **การจัดการบริการ** \> **ทั่วไป** \> **ข้อตกลงการให้บริการ** \> **ข้อตกลงการให้บริการ**</span><span class="sxs-lookup"><span data-stu-id="cb8b4-108">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="cb8b4-109">คลิกที่ **แก้ไข** เพื่อเปิดแบบฟอร์มรายละเอียด **ข้อตกลงการให้บริการ**</span><span class="sxs-lookup"><span data-stu-id="cb8b4-109">Click **Edit** to open the **Service agreements** details form.</span></span>

3.  <span data-ttu-id="cb8b4-110">ใน **บานหน้าต่างการดำเนินการ** คลิก **วัตถุที่ให้บริการ** เพื่อเปิดแบบฟอร์ม **วัตถุที่ให้บริการ**</span><span class="sxs-lookup"><span data-stu-id="cb8b4-110">On the **Action Pane**, click **Service objects** to open the **Service objects** form.</span></span>

4.  <span data-ttu-id="cb8b4-111">เลือกออบเจ็กต์ที่จะอัพเดตรายการ BOM และจากนั้นให้คลิก **ผู้ออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="cb8b4-111">Select the object to update a BOM line for, and then click **Designer**.</span></span>

5.  <span data-ttu-id="cb8b4-112">ในแบบฟอร์ม **ผู้ออกแบบ** ให้เลือกรายการ BOM ที่จะอัพเดต แล้วคลิก **แก้ไขรายการ BOM**</span><span class="sxs-lookup"><span data-stu-id="cb8b4-112">In the **Designer** form, select the BOM line to update, and then click **Edit BOM line**.</span></span>
    
    > [!NOTE]
    > <P><span data-ttu-id="cb8b4-113">บนแท็บ <STRONG>ตั้งค่า</STRONG> ให้เลือกกล่องกาเครื่องหมาย <STRONG>แก้ไขเมื่อเพิ่ม</STRONG> ถ้าคุณต้องการเปิดแบบฟอร์ม <STRONG>แก้ไขรายการ BOM</STRONG> เมื่อคุณลากเส้นลงใน BOM การบริการ</span><span class="sxs-lookup"><span data-stu-id="cb8b4-113">On the <STRONG>Setup</STRONG> tab, select the <STRONG>Edit when adding</STRONG> check box if you want the <STRONG>Edit BOM line</STRONG> form to open when you drag a line into the service BOM.</span></span></P>

6.  <span data-ttu-id="cb8b4-114">ในฟิลด์ **ปริมาณ** ป้อนปริมาณ</span><span class="sxs-lookup"><span data-stu-id="cb8b4-114">In the **Quantity** field, enter the quantity.</span></span>

7.  <span data-ttu-id="cb8b4-115">ถ้าคุณต้องการสร้างรายการใบสั่งบริการสำหรับสินค้าทดแทน ซึ่งจะสามารถออกใบแจ้งหนี้ได้ เลือกกล่องกาเครื่องหมาย **สร้างรายการใบสั่งบริการ**</span><span class="sxs-lookup"><span data-stu-id="cb8b4-115">If you want to create a service order line for the replacement item, which can then be invoiced, select the **Create service order line** check box.</span></span>

8.  <span data-ttu-id="cb8b4-116">คลิก **ตกลง** เพื่อปิดฟอร์ม</span><span class="sxs-lookup"><span data-stu-id="cb8b4-116">Click **OK** to close the form.</span></span>

## <a name="delete-a-service-bom-line"></a><span data-ttu-id="cb8b4-117">ลบรายการ BOM การบริการ</span><span class="sxs-lookup"><span data-stu-id="cb8b4-117">Delete a service BOM line</span></span>

1.  <span data-ttu-id="cb8b4-118">คลิก **การจัดการบริการ** \> **ทั่วไป** \> **ข้อตกลงการให้บริการ** \> **ข้อตกลงการให้บริการ**</span><span class="sxs-lookup"><span data-stu-id="cb8b4-118">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="cb8b4-119">คลิกที่ **แก้ไข** เพื่อเปิดแบบฟอร์มรายละเอียด **ข้อตกลงการให้บริการ**</span><span class="sxs-lookup"><span data-stu-id="cb8b4-119">Click **Edit** to open the **Service agreements** details form.</span></span>

3.  <span data-ttu-id="cb8b4-120">ใน **บานหน้าต่างการดำเนินการ** คลิก **วัตถุที่ให้บริการ** เพื่อเปิดแบบฟอร์ม **วัตถุที่ให้บริการ**</span><span class="sxs-lookup"><span data-stu-id="cb8b4-120">On the **Action Pane**, click **Service objects** to open the **Service objects** form.</span></span>

4.  <span data-ttu-id="cb8b4-121">เลือกออบเจ็กต์ที่จะลบรายการ BOM การบริการ และจากนั้นให้คลิก **ผู้ออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="cb8b4-121">Select the object to delete a service BOM line from, and then click **Designer**.</span></span>

5.  <span data-ttu-id="cb8b4-122">ในแบบฟอร์ม **ผู้ออกแบบ** ให้เลือกรายการ BOM ที่จะลบ แล้วคลิก **ลบรายการ BOM**</span><span class="sxs-lookup"><span data-stu-id="cb8b4-122">In the **Designer** form, select the BOM line to delete, and then click **Delete BOM line**.</span></span>

## <a name="see-also"></a><span data-ttu-id="cb8b4-123">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="cb8b4-123">See also</span></span>

[<span data-ttu-id="cb8b4-124">BOM เท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="cb8b4-124">Template BOMs</span></span>](template-boms.md)

  


