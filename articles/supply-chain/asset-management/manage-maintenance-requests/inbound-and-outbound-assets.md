---
title: สินทรัพย์ขาเข้าและขาออก
description: หัวข้อนี้จะอธิบายวิธีการลงทะเบียนสินทรัพย์ขาเข้าและขาออกในการจัดการสินทรัพย์
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetOutboundObjectsListPage, EntAssetOutboundObjectsDeliver, EntAssetInboundObjectsListPage, EntAssetInboundObjectsRecieve
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1a2bac914330058400a7e4d7d355bd4a00a4522f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816807"
---
# <a name="inbound-and-outbound-assets"></a><span data-ttu-id="e0323-103">สินทรัพย์ขาเข้าและขาออก</span><span class="sxs-lookup"><span data-stu-id="e0323-103">Inbound and outbound assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="e0323-104">ถ้าบริษัทของคุณทำงานซ่อมแซมหรืองานบำรุงรักษาในสินทรัพย์ที่ได้รับจากสถานที่หรือลูกค้าอื่นๆ การจัดการสินทรัพย์สามารถติดตามทั้งสินทรัพย์ขาเข้าที่อยู่ระหว่างทางไปยังบริษัทของคุณ และสินทรัพย์ขาออกที่มีการส่งคืน</span><span class="sxs-lookup"><span data-stu-id="e0323-104">If your company does repair jobs or maintenance jobs on assets that are received from other locations or customers, Asset Management can track both inbound assets that are on their way to your company and outbound assets that are being returned.</span></span>

> [!NOTE]
> <span data-ttu-id="e0323-105">ถ้าคุณต้องการใช้สถานะรอบการทำงานขาเข้าและขาออกเพื่อจัดการสินทรัพย์ที่เข้ามาและถูกส่งกลับ คุณต้องตั้งค่าสถานะของวงจรการใช้ของคำขอการบำรุงรักษาและแบบจำลองวงจรการใช้งานเพื่อสนับสนุนการดำเนินการเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="e0323-105">If you want to use inbound and outbound lifecycle states to manage assets that are coming in and being returned, you must set up maintenance request lifecycle states and lifecycle models to support these actions.</span></span> <span data-ttu-id="e0323-106">สำหรับข้อมูลเพิ่มเติม โปรดดูที่ [คำขอการบำรุงรักษา](../setup-for-maintenance-requests/requests.md)</span><span class="sxs-lookup"><span data-stu-id="e0323-106">For more information, see [Maintenance requests](../setup-for-maintenance-requests/requests.md).</span></span>

<span data-ttu-id="e0323-107">การตั้งค่าการจัดการสินทรัพย์จะกำหนดว่าคุณสามารถทำงานกับสินทรัพย์ขาเข้าและขาออกได้หรือไม่</span><span class="sxs-lookup"><span data-stu-id="e0323-107">The setup of Asset Management determines whether you can work with inbound and outbound assets.</span></span>

## <a name="register-assets-as-inbound"></a><span data-ttu-id="e0323-108">ลงทะเบียนสินทรัพย์เป็นขาเข้า</span><span class="sxs-lookup"><span data-stu-id="e0323-108">Register assets as inbound</span></span>

1. <span data-ttu-id="e0323-109">เลือก **การจัดการสินทรัพย์** \> **ทั่วไป** \> **คำขอการบำรุงรักษา** \> **คำขอการบำรุงรักษาที่ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="e0323-109">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="e0323-110">เลือกคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="e0323-110">Select the maintenance request.</span></span>
3. <span data-ttu-id="e0323-111">เลือก **ปรับปรุงสถานะคำขอการบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="e0323-111">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="e0323-112">เลือก **ขาเข้า** (หรือสถานะของวงจรการใช้อื่นที่คุณสร้างไว้สำหรับสินทรัพย์ขาเข้า) และจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="e0323-112">Select **Inbound** (or another lifecycle state that you've created for inbound assets), and then select **OK**.</span></span>

![ลงทะเบียนสินทรัพย์เป็นขาเข้า](media/07-manage-maintenance-requests.png)

## <a name="register-inbound-assets-as-received"></a><span data-ttu-id="e0323-114">ลงทะเบียนสินทรัพย์ขาเข้าเป็นได้รับแล้ว</span><span class="sxs-lookup"><span data-stu-id="e0323-114">Register inbound assets as received</span></span>

1. <span data-ttu-id="e0323-115">เลือก **การจัดการสินทรัพย์** \> **ทั่วไป** \> **ขาเข้า/ขาออก** \> **สินทรัพย์ขาเข้า**</span><span class="sxs-lookup"><span data-stu-id="e0323-115">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Inbound assets**.</span></span>
2. <span data-ttu-id="e0323-116">เลือกสินทรัพย์หรือคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="e0323-116">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="e0323-117">เลือก **ได้รับสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="e0323-117">Select **Receive assets**.</span></span>
4. <span data-ttu-id="e0323-118">ในฟิลด์ **ได้รับ** ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="e0323-118">In the **Received** field, enter the date and time.</span></span> <span data-ttu-id="e0323-119">จากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="e0323-119">Then select **OK**.</span></span> <span data-ttu-id="e0323-120">เรกคอร์ดจะถูกลบออกจากหน้ารายการ **สินทรัพย์ขาเข้า**</span><span class="sxs-lookup"><span data-stu-id="e0323-120">The record is removed from the **Inbound assets** list page.</span></span>

![ลงทะเบียนสินทรัพย์ขาเข้าเป็นได้รับแล้ว](media/08-manage-maintenance-requests.png)

## <a name="register-assets-as-outbound"></a><span data-ttu-id="e0323-122">ลงทะเบียนสินทรัพย์เป็นขาออก</span><span class="sxs-lookup"><span data-stu-id="e0323-122">Register assets as outbound</span></span>

<span data-ttu-id="e0323-123">เมื่อคุณเสร็จสิ้นการบำรุงรักษาหรืองานซ่อมแซมแล้ว คุณสามารถลงทะเบียนสินทรัพย์เป็นส่งคืนแล้ว</span><span class="sxs-lookup"><span data-stu-id="e0323-123">When you've completed the maintenance or repair job, you can register the asset as returned.</span></span>

1. <span data-ttu-id="e0323-124">เลือก **การจัดการสินทรัพย์** \> **ทั่วไป** \> **คำขอการบำรุงรักษา** \> **คำขอการบำรุงรักษาที่ใช้งานอยู่**</span><span class="sxs-lookup"><span data-stu-id="e0323-124">Select **Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.</span></span>
2. <span data-ttu-id="e0323-125">เลือกคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="e0323-125">Select the maintenance request.</span></span>
3. <span data-ttu-id="e0323-126">เลือก **ปรับปรุงสถานะคำขอการบำรุงรักษา**</span><span class="sxs-lookup"><span data-stu-id="e0323-126">Select **Update maintenance request state**.</span></span>
4. <span data-ttu-id="e0323-127">เลือก **ขาออก** (หรือสถานะของวงจรการใช้อื่นที่คุณสร้างไว้สำหรับสินทรัพย์ขาออก) และจากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="e0323-127">Select **Outbound** (or another lifecycle state that you've created for outbound assets), and then select **OK**.</span></span>

## <a name="register-outbound-assets-as-delivered"></a><span data-ttu-id="e0323-128">ลงทะเบียนสินทรัพย์ขาออกเป็นจัดส่งแล้ว</span><span class="sxs-lookup"><span data-stu-id="e0323-128">Register outbound assets as delivered</span></span>

1. <span data-ttu-id="e0323-129">เลือก **การจัดการสินทรัพย์** \> **ทั่วไป** \> **ขาเข้า/ขาออก** \> **สินทรัพย์ขาออก**</span><span class="sxs-lookup"><span data-stu-id="e0323-129">Select **Asset management** \> **Common** \> **Inbound/outbound** \> **Outbound assets**.</span></span>
2. <span data-ttu-id="e0323-130">เลือกสินทรัพย์หรือคำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="e0323-130">Select the asset or maintenance request.</span></span>
3. <span data-ttu-id="e0323-131">เลือก **จัดส่งสินทรัพย์**</span><span class="sxs-lookup"><span data-stu-id="e0323-131">Select **Deliver assets**.</span></span>
4. <span data-ttu-id="e0323-132">ในฟิลด์ **จัดส่งแล้ว** ป้อนวันที่และเวลา</span><span class="sxs-lookup"><span data-stu-id="e0323-132">In the **Delivered** field, enter the date and time.</span></span> <span data-ttu-id="e0323-133">จากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="e0323-133">Then select **OK**.</span></span> <span data-ttu-id="e0323-134">เรกคอร์ดจะถูกลบออกจากหน้ารายการ **สินทรัพย์ขาออก**</span><span class="sxs-lookup"><span data-stu-id="e0323-134">The record is removed from the **Outbound assets** list page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]