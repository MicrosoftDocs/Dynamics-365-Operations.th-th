---
title: การสร้างใบสั่งบริการด้วยตนเอง
description: คุณสามารถสร้างใบสั่งบริการด้วยตนเองได้โดยใช้ข้อตกลงการให้บริการ หรือโดยใช้แบบฟอร์ม **ใบสั่งบริการ**
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 72b600bc59119a6304fa043240a34051435f8691
ms.sourcegitcommit: 34b8f6f5c6134b7b97a9fb41d0b2e63215c67062
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470964"
---
# <a name="create-service-orders-manually"></a><span data-ttu-id="66f41-103">การสร้างใบสั่งบริการด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="66f41-103">Create service orders manually</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="66f41-104">คุณสามารถสร้างใบสั่งบริการด้วยตนเองได้โดยใช้ข้อตกลงการให้บริการ หรือโดยใช้แบบฟอร์ม **ใบสั่งบริการ**</span><span class="sxs-lookup"><span data-stu-id="66f41-104">You can create service orders manually by using a service agreement or by using the **Service orders** form.</span></span> <span data-ttu-id="66f41-105">คุณยังสามารถสร้างใบสั่งบริการจากโครงการได้ด้วย</span><span class="sxs-lookup"><span data-stu-id="66f41-105">You can also create a service order from a project.</span></span>

> [!TIP]
> <P><span data-ttu-id="66f41-106">คุณสามารถใช้กระบวนการแบบอัตโนมัติเพื่อสร้างใบสั่งบริการได้</span><span class="sxs-lookup"><span data-stu-id="66f41-106">You can use automated processes to create service orders.</span></span> 

## <a name="create-a-service-order-manually-from-a-service-agreement"></a><span data-ttu-id="66f41-107">สร้างใบสั่งบริการด้วยตนเองจากข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="66f41-107">Create a service order manually from a service agreement</span></span>

1.  <span data-ttu-id="66f41-108">เลือก **การจัดการบริการ** \> **ทั่วไป** \> **ข้อตกลงการให้บริการ** \> **ข้อตกลงการให้บริการ**</span><span class="sxs-lookup"><span data-stu-id="66f41-108">Select **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="66f41-109">เลือกข้อตกลงการให้บริการ หรือสร้างข้อตกลงการให้บริการใหม่</span><span class="sxs-lookup"><span data-stu-id="66f41-109">Select a service agreement or create a new service agreement.</span></span>

3.  <span data-ttu-id="66f41-110">เลือกแท็บ **ส่ง** และในกลุ่ม **สร้าง** เลือก **ใบสั่งบริการที่วางแผนไว้** เพื่อเปิดฟอร์ม **สร้างใบสั่งบริการ**</span><span class="sxs-lookup"><span data-stu-id="66f41-110">Select the **Deliver** tab and in the **Create** group select **Planned service orders** to open the **Create service orders** form.</span></span>

## <a name="create-a-service-order-manually-in-the-service-orders-form"></a><span data-ttu-id="66f41-111">การสร้างใบสั่งบริการด้วยตนเองในแบบฟอร์มใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="66f41-111">Create a service order manually in the Service orders form</span></span>

1.  <span data-ttu-id="66f41-112">เลือก **การจัดการบริการ** \> **ทั่วไป** \> **ใบสั่งบริการ** \> **ใบสั่งบริการ**</span><span class="sxs-lookup"><span data-stu-id="66f41-112">Select **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="66f41-113">เลือก **สร้าง** เพื่อสร้างใบสั่งบริการใหม่</span><span class="sxs-lookup"><span data-stu-id="66f41-113">Select **New** to create a new service order.</span></span>

3.  <span data-ttu-id="66f41-114">สร้างบรรทัดใบสั่งบริการสำหรับใบสั่งบริการนั้น</span><span class="sxs-lookup"><span data-stu-id="66f41-114">Create service order lines for the service order.</span></span>

> [!NOTE]
> <P><span data-ttu-id="66f41-115">ถ้ามีการเลือกกล่องกาเครื่องหมาย <STRONG>อนุญาตให้ใช้ได้โดยไม่มีข้อตกลงการให้บริการ</STRONG> ในแบบฟอร์ม <STRONG>พารามิเตอร์การจัดการงานบริการ</STRONG> คุณจะสามารถลงรายการบัญชีธุรกรรมได้จากรายการใบสั่งบริการโดยไม่ต้องแนบใบสั่งบริการกับข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="66f41-115">If the <STRONG>Allow without service agreement</STRONG> check box in the <STRONG>Service management parameters</STRONG> form is selected, you can post the transactions from the service order lines without attaching the service order to a service agreement.</span></span> <span data-ttu-id="66f41-116">ถ้ามีการยกเลิกการเลือกกล่องกาเครื่องหมายนี้ คุณจะต้องแนบใบสั่งบริการที่สร้างด้วยตนเองกับโครงการก่อนที่จะลงรายการบัญชีบรรทัดใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="66f41-116">If the check box is cleared, you must attach the manually created service order to a project before posting the service order lines.</span></span></P>

## <a name="create-a-service-order-from-a-project"></a><span data-ttu-id="66f41-117">สร้างใบสั่งบริการจากโครงการ</span><span class="sxs-lookup"><span data-stu-id="66f41-117">Create a service order from a project</span></span>

1.  <span data-ttu-id="66f41-118">ไปยัง **การจัดการโครงการและการบัญชี** \> **ทั่วไป** \> **โครงการ** \> **โครงการทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="66f41-118">Go to **Project management and accounting** \> **Common** \> **Projects** \> **All projects**.</span></span>

2.  <span data-ttu-id="66f41-119">ในฟอร์ม **โครงการ** บน **บานหน้าต่างการดำเนินการ** เลือกแท็บ **จัดการ** \> เลือก **บริการ** \> **ใบสั่งบริการ**</span><span class="sxs-lookup"><span data-stu-id="66f41-119">In the **Projects** form, on the **Action Pane**, select the **Manage** tab \> select **Service** \> **Service orders**.</span></span>

3.  <span data-ttu-id="66f41-120">ปฏิบัติตามกระบวนงานก่อนหน้า เพื่อสร้างใบสั่งบริการด้วยตนเองจากแบบฟอร์ม **ใบสั่งบริการ**</span><span class="sxs-lookup"><span data-stu-id="66f41-120">Follow the previous procedure to create a service order manually in the **Service orders** form.</span></span> <span data-ttu-id="66f41-121">ฟิลด์ **รหัสโครงการ** แสดงข้อมูลอ้างอิงโครงการ</span><span class="sxs-lookup"><span data-stu-id="66f41-121">The **Project ID** field displays the project reference.</span></span>

> [!NOTE]
> <P><span data-ttu-id="66f41-122">ถ้ามีการเลือกกล่องกาเครื่องหมาย <STRONG>อนุญาตให้ใช้ได้โดยไม่มีข้อตกลงการให้บริการ</STRONG> ในแบบฟอร์ม <STRONG>พารามิเตอร์การจัดการงานบริการ</STRONG> คุณจะสามารถลงรายการบัญชีธุรกรรมได้จากรายการใบสั่งบริการโดยไม่ต้องแนบใบสั่งบริการกับข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="66f41-122">If the <STRONG>Allow without service agreement</STRONG> check box in the <STRONG>Service management parameters</STRONG> form is selected, you can post the transactions from the service order lines without attaching the service order to a service agreement.</span></span> <span data-ttu-id="66f41-123">ถ้ามีการยกเลิกการเลือกกล่องกาเครื่องหมายนี้ คุณจะต้องแนบใบสั่งบริการที่สร้างด้วยตนเองกับโครงการก่อนที่จะลงรายการบัญชีบรรทัดใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="66f41-123">If the check box is cleared, you must attach the manually created service order to a project before posting the service order lines.</span></span></P>

## <a name="create-a-service-order-from-the-sales-order-form"></a><span data-ttu-id="66f41-124">สร้างใบสั่งบริการจากฟอร์มใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="66f41-124">Create a service order from the Sales order form</span></span>

<span data-ttu-id="66f41-125">คุณสามารถสร้างใบสั่งบริการจากแบบฟอร์ม **ใบสั่งขาย** โดยใช้วิซาร์ด **สร้างใบสั่งบริการใหม่ตามใบสั่งขาย** ได้</span><span class="sxs-lookup"><span data-stu-id="66f41-125">You can create a service order from the **Sales orders** form by using the **Create a new service order based on the sales order** wizard.</span></span>

1.  <span data-ttu-id="66f41-126">ไปยัง **การขายและการตลาด** \> **ทั่วไป** \> **ใบสั่งขาย** \> **ใบสั่งขายทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="66f41-126">Go to **Sales and marketing** \> **Common** \> **Sales orders** \> **All sales orders**.</span></span>

2.  <span data-ttu-id="66f41-127">เปิดใบสั่งขายที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="66f41-127">Open the relevant sales order.</span></span>

3.  <span data-ttu-id="66f41-128">บนแท็บ **ใบสั่งบริการ** เลือก **ใบสั่งบริการ** เพื่อเริ่มต้นวิซาร์ด **สร้างใบสั่งบริการใหม่ตามใบสั่งขาย**</span><span class="sxs-lookup"><span data-stu-id="66f41-128">On the **Sales order** tab, select **Service order** to start the **Create a new service order based on the sales order** wizard.</span></span>

4.  <span data-ttu-id="66f41-129">เลือก **ถัดไป \>** และจากนั้น ดำเนินการขั้นตอนต่อไปนี้ให้เสร็จสมบูรณ์ในหน้า **เลือกข้อตกลงสำหรับใบสั่งบริการ**:</span><span class="sxs-lookup"><span data-stu-id="66f41-129">Select **Next \>**, and then complete the following steps on the **Select agreement for service order** page:</span></span>
    
      - <span data-ttu-id="66f41-130">ใช้ฟิลด์ **ข้อตกลงการให้บริการ** เพื่อเลือกข้อตกลงการให้บริการที่มีใบสั่งบริการใหม่ที่ควรจะสัมพันธ์ด้วย</span><span class="sxs-lookup"><span data-stu-id="66f41-130">Use the **Service agreement** field to select the service agreement with which the new service order should be associated.</span></span>
    
      - <span data-ttu-id="66f41-131">ไม่จำเป็นต้องระบุ: ใช้ฟิลด์ **รหัสโครงการ** เพื่อเชื่อมโยงใบสั่งบริการนี้กับโครงการเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="66f41-131">Optional: Use the **Project ID** field to associate this service order with a particular project.</span></span>

5.  <span data-ttu-id="66f41-132">เลือก **ถัดไป \>** และจากนั้น ดำเนินการขั้นตอนต่อไปนี้ให้เสร็จสมบูรณ์ในหน้า **สร้างใบสั่งบริการ**:</span><span class="sxs-lookup"><span data-stu-id="66f41-132">Select **Next \>**, and then complete the following steps on the **Create service order** page:</span></span>
    
      - <span data-ttu-id="66f41-133">ป้อนวันที่และเวลาสำหรับการเรียกบริการที่จะเริ่มขึ้นในฟิลด์ **เวลาการบริการที่ต้องการ**</span><span class="sxs-lookup"><span data-stu-id="66f41-133">Enter a date and time for the service call to begin in the **Preferred service time** field.</span></span>
    
      - <span data-ttu-id="66f41-134">ไม่จำเป็นต้องระบุ: แก้ไขข้อความในฟิลด์ **คำอธิบาย**</span><span class="sxs-lookup"><span data-stu-id="66f41-134">Optional: Modify the text in the **Description** field.</span></span> <span data-ttu-id="66f41-135">ตามค่าเริ่มต้น ฟิลด์นี้ประกอบด้วยคำอธิบายของข้อตกลงการให้บริการที่คุณเลือกไว้บนหน้าก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="66f41-135">By default, this field contains the description of the service agreement that you selected on the previous page.</span></span>
    
      - <span data-ttu-id="66f41-136">ในฟิลด์ **ผู้รับผิดชอบ** ให้เลือกรหัสของพนักงานซึ่งเป็นผู้รับผิดชอบข้อตกลง และถ้าคุณทราบว่าคืออะไร ให้ป้อนรหัสของช่างเทคนิคที่ต้องการของลูกค้าสำหรับการเรียกบริการ</span><span class="sxs-lookup"><span data-stu-id="66f41-136">In the **Responsible** field, select the ID of the employee who is responsible for the agreement, and if you know what it is, enter the ID of the customer's preferred technician for the service call.</span></span>
    
      - <span data-ttu-id="66f41-137">ในฟิลด์ **รหัสผู้ติดต่อ** เลือกบุคคลในบริษัทของลูกค้า ซึ่งควรจะได้รับการติดต่อเกี่ยวกับใบสั่งบริการนี้</span><span class="sxs-lookup"><span data-stu-id="66f41-137">In the **Contact ID** field, select the person in the customer's company who should be contacted regarding this service order.</span></span>

6.  <span data-ttu-id="66f41-138">เลือก **ถัดไป \>**  แล้วจากนั้น เลือก **ทำให้เสร็จสิ้น**</span><span class="sxs-lookup"><span data-stu-id="66f41-138">Select **Next \>**, and then select **Finish**.</span></span>


## <a name="see-also"></a><span data-ttu-id="66f41-139">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="66f41-139">See also</span></span>

[<span data-ttu-id="66f41-140">ใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="66f41-140">Service orders</span></span>](service-orders.md)

[<span data-ttu-id="66f41-141">สร้างใบสั่งบริการโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="66f41-141">Create service orders automatically</span></span>](create-service-orders-automatically.md)

<span data-ttu-id="66f41-142">[การสร้างใบสั่งบริการ (แบบฟอร์มคลาส)](https://technet.microsoft.com/library/aa553901\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="66f41-142">[Create service orders (class form)](https://technet.microsoft.com/library/aa553901\(v=ax.60\))</span></span> 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]