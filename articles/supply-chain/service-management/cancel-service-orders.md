---
title: "ยกเลิกใบสั่งบริการ"
description: "คุณสามารถยกเลิกใบสั่งบริการหรือรายการใบสั่งบริการได้จากตัวใบสั่งบริการเอง หรือคุณสามารถยกเลิกใบสั่งบริการหลายใบได้โดยการรันงานประจำงวด"
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 8e5ad119c28bba18b75bb5ed7854e94a4e734d55
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---

# <a name="cancel-service-orders"></a><span data-ttu-id="03a9b-103">ยกเลิกใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="03a9b-103">Cancel service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="03a9b-104">คุณสามารถยกเลิกใบสั่งบริการหรือรายการใบสั่งบริการได้จากตัวใบสั่งบริการเอง หรือคุณสามารถยกเลิกใบสั่งบริการหลายใบได้โดยการรันงานประจำงวด</span><span class="sxs-lookup"><span data-stu-id="03a9b-104">You can cancel a service order or service order line from the service order itself, or you can cancel multiple service orders by running a periodic job.</span></span>


> [!NOTE]
> <P><span data-ttu-id="03a9b-105">ใบสั่งบริการไม่สามารถยกเลิกได้ ถ้าขั้นตอนของใบสั่งบริการไม่อนุญาตการยกเลิก ถ้าใบสั่งบริการมีความต้องการสินค้า หรือถ้าใบสั่งบริการได้ถูกลงรายการบัญชีแล้ว</span><span class="sxs-lookup"><span data-stu-id="03a9b-105">Service orders cannot be canceled if the stage of the service order does not allow cancelation, if the service order has item requirements, or if the service order has already been posted.</span></span></P>


## <a name="cancel-a-service-order-in-the-service-orders-form"></a><span data-ttu-id="03a9b-106">การยกเลิกใบสั่งบริการในแบบฟอร์มใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="03a9b-106">Cancel a service order in the Service orders form</span></span>

1.  <span data-ttu-id="03a9b-107">คลิก **การจัดการบริการ** \> **ทั่วไป** \> **ใบสั่งบริการ** \> **ใบสั่งบริการ**</span><span class="sxs-lookup"><span data-stu-id="03a9b-107">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span> <span data-ttu-id="03a9b-108">เลือกใบสั่งบริการ และในบานหน้าต่างการดำเนินการ คลิก **ยกเลิกใบสั่ง**</span><span class="sxs-lookup"><span data-stu-id="03a9b-108">Select the service order, and on the Action Pane, click **Cancel order**.</span></span>

## <a name="cancel-a-service-order-line"></a><span data-ttu-id="03a9b-109">การยกเลิกบรรทัดใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="03a9b-109">Cancel a service order line</span></span>

1.  <span data-ttu-id="03a9b-110">คลิก **การจัดการบริการ** \> **ทั่วไป** \> **ใบสั่งบริการ** \> **ใบสั่งบริการ**</span><span class="sxs-lookup"><span data-stu-id="03a9b-110">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span> <span data-ttu-id="03a9b-111">ดับเบิลคลิกใบสั่งบริการที่ประกอบด้วยรายการที่คุณต้องการยกเลิก</span><span class="sxs-lookup"><span data-stu-id="03a9b-111">Double-click the service order that contains the line you want to cancel.</span></span>

2.  <span data-ttu-id="03a9b-112">เลือกรายการใบสั่งบริการที่คุณต้องการยกเลิก แล้วคลิก **ยกเลิกรายการใบสั่ง** เพื่อเปลี่ยนสถานะของรายการเป็น **ถูกยกเลิกแล้ว**</span><span class="sxs-lookup"><span data-stu-id="03a9b-112">Select the service order line that you want to cancel, and then click **Cancel order line** to change the status of the line to **Canceled**.</span></span>


> [!TIP]
> <P><span data-ttu-id="03a9b-113">ในการกลับรายการการยกเลิกของรายการใบสั่งบริการ และเปลี่ยนสถานะกลับไปเป็น <STRONG>สร้างแล้ว</STRONG> คลิก <STRONG>ถอนการยกเลิก</STRONG></span><span class="sxs-lookup"><span data-stu-id="03a9b-113">To reverse the cancellation of a service order line and change the status back to <STRONG>Created</STRONG>, click <STRONG>Revoke cancel</STRONG>.</span></span></P>


## <a name="cancel-multiple-service-orders"></a><span data-ttu-id="03a9b-114">การยกเลิกใบสั่งบริการหลายใบ</span><span class="sxs-lookup"><span data-stu-id="03a9b-114">Cancel multiple service orders</span></span>

1.  <span data-ttu-id="03a9b-115">คลิก **การจัดการบริการ** \> **งานประจำงวด** \> **ใบสั่งบริการ** \> **ยกเลิกใบสั่งบริการ**</span><span class="sxs-lookup"><span data-stu-id="03a9b-115">Click **Service management** \> **Periodic** \> **Service orders** \> **Cancel service orders**.</span></span>

2.  <span data-ttu-id="03a9b-116">คลิกปุ่ม **เลือก** </span><span class="sxs-lookup"><span data-stu-id="03a9b-116">Click the **Select** button.</span></span>

3.  <span data-ttu-id="03a9b-117">ในแบบฟอร์ม **การสอบถาม** ในคอลัมน์ **เงื่อนไข** เลือกใบสั่งบริการที่คุณต้องการยกเลิก</span><span class="sxs-lookup"><span data-stu-id="03a9b-117">In the **Inquiry** form, in the **Criteria** column, select the service orders that you want to cancel.</span></span>

4.  <span data-ttu-id="03a9b-118">คลิก **ตกลง** เพื่อปิดแบบฟอร์ม **การสอบถาม**</span><span class="sxs-lookup"><span data-stu-id="03a9b-118">Click **OK** to close the **Inquiry** form.</span></span>

5.  <span data-ttu-id="03a9b-119">เลือกกล่องกาเครื่องหมาย **แสดง Infolog** เพื่อสร้าง Infolog ซึ่งแสดงใบสั่งบริการที่ยกเลิกแล้ว</span><span class="sxs-lookup"><span data-stu-id="03a9b-119">Select the **Show Infolog** check box to generate an Infolog that lists the canceled service orders.</span></span>

6.  <span data-ttu-id="03a9b-120">เลือกกล่องกาเครื่องหมาย **เพิกถอนการยกเลิก** ถ้าคุณต้องการกลับรายการสถานะ **ยกเลิกแล้ว** ของใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="03a9b-120">Select the **Revoke cancel** check box if you want to reverse the **Canceled** status of a service order.</span></span>

7.  <span data-ttu-id="03a9b-121">คลิก **ตกลง** </span><span class="sxs-lookup"><span data-stu-id="03a9b-121">Click **OK**.</span></span>

<span data-ttu-id="03a9b-122">ใบสั่งบริการที่เลือกไว้จะถูกยกเลิก หรือสถานะความคืบหน้า **ยกเลิกแล้ว** ถูกกลับรายการเป็น **อยู่ระหว่างดำเนินการ**</span><span class="sxs-lookup"><span data-stu-id="03a9b-122">The selected service orders are either canceled or their progress status of **Canceled** has been reversed to **In process**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="03a9b-123">ถ้าคุณเลือกกล่องกาเครื่องหมาย <STRONG>เพิกถอนการยกเลิก</STRONG> ใบสั่งบริการที่มีสถานะความคืบหน้าเป็น <STRONG>ยกเลิกแล้ว</STRONG> จะถูกกลับรายการ และไม่มีการยกเลิกใบสั่งบริการที่มีสถานะความคืบหน้าเป็น <STRONG>อยู่ระหว่างดำเนินการ</STRONG></span><span class="sxs-lookup"><span data-stu-id="03a9b-123">If you select the <STRONG>Revoke cancel</STRONG> check box, service orders with a progress status of <STRONG>Canceled</STRONG> are reversed and service orders with a progress status of <STRONG>In process</STRONG> are not canceled.</span></span></P>


  



