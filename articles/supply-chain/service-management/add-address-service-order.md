---
title: เพิ่มที่อยู่ลงในใบสั่งบริการ
description: 'หัวข้อนี้อธิบายวิธีการเพิ่มที่อยู่ของลูกค้าไปยังใบสั่งบริการ '
author: ShylaThompson
manager: tfehr
ms.date: 05/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7b9c6a410acbfebb3a83e753c422dd87dbf52566
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205868"
---
# <a name="add-an-address-to-a-service-order"></a><span data-ttu-id="ad253-103">เพิ่มที่อยู่ลงในใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="ad253-103">Add an address to a service order</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="ad253-104">หัวข้อนี้อธิบายวิธีการเพิ่มที่อยู่ของลูกค้าไปยังใบสั่งบริการ </span><span class="sxs-lookup"><span data-stu-id="ad253-104">This topic describes how to add a customer address to a service order.</span></span> <span data-ttu-id="ad253-105">เมื่อคุณสร้างใบสั่งบริการ ข้อมูลที่อยู่จะถูกโอนย้ายจากโครงการที่แนบใบสั่งบริการไว้ </span><span class="sxs-lookup"><span data-stu-id="ad253-105">When you create a service order, the address information is transferred from the project that the service order is attached to.</span></span> <span data-ttu-id="ad253-106">อย่างไรก็ตาม คุณสามารถเลือกตำแหน่งที่ตั้งทางเลือกได้จากที่อยู่ที่ถูกป้อนไว้แล้วใน Microsoft Dynamics AX สำหรับลูกค้า ผู้จัดจำหน่าย ไซต์ คลังสินค้า ใบสั่งบริการ และโครงการ</span><span class="sxs-lookup"><span data-stu-id="ad253-106">However, you can select an alternative location from addresses that are already entered in Microsoft Dynamics AX for customers, vendors, sites, warehouses, service orders, and projects.</span></span>

<span data-ttu-id="ad253-107">คุณยังสามารถสร้างที่อยู่ใหม่โดยค่าเริ่มต้น </span><span class="sxs-lookup"><span data-stu-id="ad253-107">You can also create a new address.</span></span> <span data-ttu-id="ad253-108">ที่อยู่ใหม่จะถูกโอนย้ายไปยังโครงการ </span><span class="sxs-lookup"><span data-stu-id="ad253-108">By default, the new address is transferred to the project.</span></span> <span data-ttu-id="ad253-109">อย่างไรก็ตาม คุณสามารถระบุว่าที่อยู่ใหม่จะเกี่ยวข้องกับอินสแตนซ์นี้ของบริการเท่านั้น </span><span class="sxs-lookup"><span data-stu-id="ad253-109">However, you can specify that the new address is only relevant for this instance of the service.</span></span> <span data-ttu-id="ad253-110">หากคุณทำที่อยู่ใหม่จะไม่มีการโอนย้ายไปยังโครงการ</span><span class="sxs-lookup"><span data-stu-id="ad253-110">If you do, the new address is not transferred to the project.</span></span>

## <a name="create-a-customer-address-for-a-service-order"></a><span data-ttu-id="ad253-111">สร้างที่อยู่ลูกค้าสำหรับใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="ad253-111">Create a customer address for a service order</span></span>

<span data-ttu-id="ad253-112">ในการเพิ่มที่อยู่ในรายการใบสั่งบริการ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="ad253-112">To add an address to a service order, follow these steps:</span></span>

1.  <span data-ttu-id="ad253-113">คลิก **การจัดการบริการ** \> **ทั่วไป** \> **ใบสั่งบริการ** \> **ใบสั่งบริการ**</span><span class="sxs-lookup"><span data-stu-id="ad253-113">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="ad253-114">เปิดใบสั่งบริการที่คุณต้องการสร้างที่อยู่</span><span class="sxs-lookup"><span data-stu-id="ad253-114">Open the service order that you want to create an address for.</span></span>

3.  <span data-ttu-id="ad253-115">บน **บานหน้าต่างการดำเนินการ** คลิก **แก้ไข** แล้วคลิก **มุมมองหัวข้อ**</span><span class="sxs-lookup"><span data-stu-id="ad253-115">On the **Action Pane**, click **Edit**, and then click **Header view**.</span></span>

4.  <span data-ttu-id="ad253-116">บน FastTab **ที่อยู่** คลิก **เพิ่มที่อยู่**</span><span class="sxs-lookup"><span data-stu-id="ad253-116">On the **Address** FastTab, click **Add address**.</span></span>

5.  <span data-ttu-id="ad253-117">ในแบบฟอร์ม **ที่อยู่ใหม่** ป้อนชื่อเฉพาะสำหรับที่อยู่และดำเนินการฟิลด์ที่เหลือให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="ad253-117">In the **New address** form, enter a unique name for the address and complete the remaining fields.</span></span> 
    

    > [!WARNING]
    > <P><span data-ttu-id="ad253-118">ถ้าคุณป้อนชื่อเดียวกันเป็นอยู่ที่มีอยู่ ข้อมูลที่คุณป้อนในฟิลด์ที่เหลือจะเขียนทับข้อมูลสำหรับที่อยู่ที่มีอยู่</span><span class="sxs-lookup"><span data-stu-id="ad253-118">If you enter the same name as an existing address, the information that you enter in the remaining fields will overwrite information for the existing address.</span></span></P>


6.  <span data-ttu-id="ad253-119">คลิก **ตกลง** เพื่อคัดลอกที่อยู่ใหม่ลงในใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="ad253-119">Click **OK** to copy the new address to your service order.</span></span>

## <a name="specify-an-alternative-address-on-a-service-order"></a><span data-ttu-id="ad253-120">ระบุที่อยู่อื่นๆ ในใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="ad253-120">Specify an alternative address on a service order</span></span>

<span data-ttu-id="ad253-121">ในการเพิ่มที่อยู่สำรองในรายการใบสั่งบริการ ให้ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="ad253-121">To add an alternative address to a service order, follow these steps:</span></span>

1.  <span data-ttu-id="ad253-122">คลิก **การจัดการบริการ** \> **ทั่วไป** \> **ใบสั่งบริการ** \> **ใบสั่งบริการ**</span><span class="sxs-lookup"><span data-stu-id="ad253-122">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="ad253-123">เปิดใบสั่งบริการที่คุณต้องการป้อนที่อยู่สำรอง</span><span class="sxs-lookup"><span data-stu-id="ad253-123">Open the service order that you want to enter an alternative address for.</span></span>

3.  <span data-ttu-id="ad253-124">บน **บานหน้าต่างการดำเนินการ** คลิก **แก้ไข** แล้วคลิก **มุมมองหัวข้อ**</span><span class="sxs-lookup"><span data-stu-id="ad253-124">On the **Action Pane**, click **Edit**, and then click **Header view**.</span></span>

4.  <span data-ttu-id="ad253-125">บน FastTab **ที่อยู่** คลิก **ที่อยู่อื่น**</span><span class="sxs-lookup"><span data-stu-id="ad253-125">On the **Address** FastTab, click **Other address**.</span></span>

5.  <span data-ttu-id="ad253-126">ในฟอร์ม **การเลือกที่อยู่** ในฟิลด์ **ชนิดของเรกคอร์ด** เลือก **ใบสั่งบริการ**</span><span class="sxs-lookup"><span data-stu-id="ad253-126">In the **Address selection** form, in the **Record type** field, select **Service orders**.</span></span>

6.  <span data-ttu-id="ad253-127">เลือกที่อยู่ แล้วคลิก **ตกลง** เพื่อคัดลอกลงในใบสั่งบริการ</span><span class="sxs-lookup"><span data-stu-id="ad253-127">Select an address, and then click **OK** to copy it to your service order.</span></span>


  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]