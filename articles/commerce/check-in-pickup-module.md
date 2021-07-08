---
title: เช็คอินโมดูลการเบิกสินค้า
description: หัวข้อนี้อธิบายโมดูลเช็คอินสำหรับการเบิก และอธิบายวิธีการตั้งค่าคอนฟิกใน Microsoft Dynamics 365 Commerce
author: bicyclingfool
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 0baa922afc72778dd6e4836398a280cbe6abaec2
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270594"
---
# <a name="check-in-for-pickup-module"></a><span data-ttu-id="42dd8-103">เช็คอินโมดูลการเบิกสินค้า</span><span class="sxs-lookup"><span data-stu-id="42dd8-103">Check-in for pickup module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="42dd8-104">หัวข้อนี้อธิบายโมดูลเช็คอินสำหรับการเบิก และอธิบายวิธีการตั้งค่าคอนฟิกใน Microsoft Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="42dd8-104">This topic covers the check-in for pickup module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="42dd8-105">โมดูลการเช็คอินสำหรับเบิกสินค้าจะมีหน้าการยืนยันของลูกค้าที่ใช้ ความสามารถในการเช็คอินของลูกค้า Dynamics 365 Commerce เพื่อแจ้งให้ร้านค้าทราบเกี่ยวกับการมาถึงของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="42dd8-105">The check-in for pickup module provides a confirmation page for customers who use the Dynamics 365 Commerce customer check-in capabilities to notify a store about their arrival.</span></span> <span data-ttu-id="42dd8-106">โมดูลรเช็คอินการเบิกสินค้ายังช่วยให้คุณสามารถตั้งค่าคอนฟิกแบบฟอร์มที่รวบรวมข้อมูลเพิ่มเติมจากลูกค้า เพื่อช่วยในการจัดส่งใบสั่งอีกด้วย</span><span class="sxs-lookup"><span data-stu-id="42dd8-106">The check-in for pickup module also lets you configure a form that collects additional information from customers to facilitate order delivery.</span></span> <span data-ttu-id="42dd8-107">ข้อมูลนี้รวมถึงหมายเลขจุดจอดรถของลูกค้า และรุ่นของรถยนต์</span><span class="sxs-lookup"><span data-stu-id="42dd8-107">This information includes a customer's parking spot number, and the make and model of their vehicle.</span></span> 

## <a name="module-properties"></a><span data-ttu-id="42dd8-108">คุณสมบัติของโมดูล</span><span class="sxs-lookup"><span data-stu-id="42dd8-108">Module properties</span></span>

| <span data-ttu-id="42dd8-109">ชื่อคุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="42dd8-109">Property name</span></span> | <span data-ttu-id="42dd8-110">มูลค่า</span><span class="sxs-lookup"><span data-stu-id="42dd8-110">Values</span></span> | <span data-ttu-id="42dd8-111">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="42dd8-111">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="42dd8-112">ข้อความยืนยัน</span><span class="sxs-lookup"><span data-stu-id="42dd8-112">Confirmation text</span></span> | <span data-ttu-id="42dd8-113">สตริงข้อความ</span><span class="sxs-lookup"><span data-stu-id="42dd8-113">Text string</span></span> | <span data-ttu-id="42dd8-114">เนื้อหาของหัวข้อที่ปรากฏบนหน้าการยืนยันการเช็คอิน</span><span class="sxs-lookup"><span data-stu-id="42dd8-114">Content for the heading that appears on the check-in confirmation page.</span></span> |
| <span data-ttu-id="42dd8-115">แสดงคิวอาร์โค้ด</span><span class="sxs-lookup"><span data-stu-id="42dd8-115">Show QR code</span></span> | <span data-ttu-id="42dd8-116">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="42dd8-116">**True** or **False**</span></span> | <span data-ttu-id="42dd8-117">เมื่อตั้งค่าคุณสมบัตินี้เป็น **จริง** หน้าการยืนยันการเช็คอินแสดงคิวอาร์โค้อ ที่แสดงถึงรหัสการยืนยันใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="42dd8-117">When this property is set to **True**, the check-in confirmation page shows a QR code that represents the order confirmation ID.</span></span> |
| <span data-ttu-id="42dd8-118">หัวข้อข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="42dd8-118">Additional information heading</span></span> | <span data-ttu-id="42dd8-119">สตริงข้อความ</span><span class="sxs-lookup"><span data-stu-id="42dd8-119">Text string</span></span> | <span data-ttu-id="42dd8-120">เนื้อหาเป็นหัวข้อที่จะปรากฏขึ้นเมื่อตั้งค่าคอนฟิกฟิลด์ข้อมูลเพิ่มเติมแล้ว</span><span class="sxs-lookup"><span data-stu-id="42dd8-120">Content for the heading that appears when additional information fields have been configured.</span></span> |
| <span data-ttu-id="42dd8-121">คีย์ข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="42dd8-121">Additional information keys</span></span> | <span data-ttu-id="42dd8-122">คู่รหัสทรัพยากร/ค่าทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="42dd8-122">Resource ID/resource value pair</span></span> | <span data-ttu-id="42dd8-123">แต่ละคีย์จะสร้างฟิลด์แบบฟอร์มและป้ายชื่อที่เกี่ยวข้อง ที่ใช้เพื่อรวบรวมข้อมูลเพิ่มเติมจากลูกค้า</span><span class="sxs-lookup"><span data-stu-id="42dd8-123">Each key creates a form field and an associated label that are used to collect additional information from customers.</span></span> |
| <span data-ttu-id="42dd8-124">คีย์ข้อมูลเพิ่มเติม \> รหัสทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="42dd8-124">Additional information keys \> Resource ID</span></span> | <span data-ttu-id="42dd8-125">สตริงข้อความ</span><span class="sxs-lookup"><span data-stu-id="42dd8-125">Text string</span></span> | <span data-ttu-id="42dd8-126">แต่ละคีย์ข้อมูลจะสร้างฟิลด์แบบฟอร์มและป้ายชื่อที่เกี่ยวข้อง ที่ใช้เพื่อรวบรวมข้อมูลเพิ่มเติมจากลูกค้า</span><span class="sxs-lookup"><span data-stu-id="42dd8-126">Each information key creates a form field and an associated label that are used to collect additional information from customers.</span></span> <span data-ttu-id="42dd8-127">คุณสมบัตินี้จะระบุคีย์ข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="42dd8-127">This property identifies the additional information key.</span></span> <span data-ttu-id="42dd8-128">ในงานที่สร้างใน การขายหน้าร้าน (POS) ค่าของคุณสมบัตินี้จะแสดงเป็นป้ายชื่อในฟิลด์คําแนะนํา</span><span class="sxs-lookup"><span data-stu-id="42dd8-128">In the task that is created in point of sale (POS), the value of this property is shown as the label in the instructions field.</span></span> |
| <span data-ttu-id="42dd8-129">คีย์ข้อมูลเพิ่มเติม \> ค่าทรัพยากร</span><span class="sxs-lookup"><span data-stu-id="42dd8-129">Additional information keys \> Resource value</span></span> | <span data-ttu-id="42dd8-130">สตริงข้อความ</span><span class="sxs-lookup"><span data-stu-id="42dd8-130">Text string</span></span> | <span data-ttu-id="42dd8-131">ป้ายสำหรับฟิลด์ข้อความในงานใน POS</span><span class="sxs-lookup"><span data-stu-id="42dd8-131">The label for the text field in the task in POS.</span></span> |
| <span data-ttu-id="42dd8-132">คีย์ข้อมูลเพิ่มเติม \> จำเป็น</span><span class="sxs-lookup"><span data-stu-id="42dd8-132">Additional information keys \> Required</span></span> | <span data-ttu-id="42dd8-133">**จริง** หรือ **เท็จ**</span><span class="sxs-lookup"><span data-stu-id="42dd8-133">**True** or **False**</span></span> | <span data-ttu-id="42dd8-134">คุณสมบัตินี้จะระบุว่าลูกค้าต้องกรอกข้อมูลในฟิลด์แบบฟอร์มก่อน จึงจะสามารถต่อไปหรือไม่</span><span class="sxs-lookup"><span data-stu-id="42dd8-134">This property specifies whether customers must fill in the form field before they can continue.</span></span> <span data-ttu-id="42dd8-135">เมื่อตั้งค่าคุณสมบัตินี้เป็น **จริง** เครื่องหมายดอกจันจะแสดงถัดจากป้ายชื่อแบบฟอร์ม และทําการตรวจสอบที่เป็น null เพื่อป้องกันไม่ให้ลูกค้าไปต่อ ถ้าไม่มีการป้อนค่า</span><span class="sxs-lookup"><span data-stu-id="42dd8-135">When this property is set to **True**, an asterisk is rendered next to the form label, and a null check is done to prevent customers from continuing if no value is entered.</span></span> |

## <a name="add-the-check-in-for-pickup-module-to-a-page"></a><span data-ttu-id="42dd8-136">เพิ่มโมดูลเช็คอินเพื่อเบิกสินค้า ลงในหน้า</span><span class="sxs-lookup"><span data-stu-id="42dd8-136">Add the check-in for pickup module to a page</span></span>

<span data-ttu-id="42dd8-137">ควรเพิ่มโมดูลเช็คอินเพื่อเบิกสินค้าเข้าในหน้าใหม่ที่คุณสร้าง เพื่อยืนยันการเช็คอิน</span><span class="sxs-lookup"><span data-stu-id="42dd8-137">The check-in for pickup module should be added to the new page that you create for check-in confirmation.</span></span> <span data-ttu-id="42dd8-138">หน้านี้จะหน้าที่เป็นประสบการณ์การยืนยันการเช็คอินของลูกค้าที่เลือกลิงค์หรือปุ่ม **ฉันอยู่ที่นี่** ในอีเมลของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="42dd8-138">That page will serve as the check-in confirmation experience for customers who select the **I am here** link or button in their email.</span></span> 

## <a name="configure-the-additional-information-form"></a><span data-ttu-id="42dd8-139">ตั้งค่าคอนฟิกแบบฟอร์มข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="42dd8-139">Configure the additional information form</span></span>

<span data-ttu-id="42dd8-140">ตามค่าเริ่มต้น ถ้าไม่มีการตั้งค่าคอนฟิกคีย์ข้อมูลเพิ่มเติมใดๆ โมดูลจะแสดงหน้าการยืนยันการเช็คอินของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="42dd8-140">By default, if no additional information keys are configured, the module shows customers the check-in confirmation page.</span></span> <span data-ttu-id="42dd8-141">ตามการยืนยันการเช็คอินจะแสดงขึ้น งานจะถูกสร้างขึ้นใน POS ของร้านค้าที่จะเบิกสินค้าตามใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="42dd8-141">As the check-in confirmation is shown, a task is created in POS for the store where the order is being picked up.</span></span>

<span data-ttu-id="42dd8-142">เมื่อตั้งค่าคอนฟิกคีย์ข้อมูลเพิ่มเติมหนึ่งคีย์หรือมากกว่านั้น ลูกค้าจะได้รับพร้อมต์เพื่อป้อนข้อมูลก่อน</span><span class="sxs-lookup"><span data-stu-id="42dd8-142">When one or more additional information keys are configured, customers are first prompted to enter information.</span></span> <span data-ttu-id="42dd8-143">เมื่อเลือก **ส่ง** ระบบจะแสดงการยืนยันการเช็คอิน และสร้างงานใน POS</span><span class="sxs-lookup"><span data-stu-id="42dd8-143">When they select **Submit**, they are shown the check-in confirmation, and a task is created in POS.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="42dd8-144">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="42dd8-144">Additional resources</span></span>

[<span data-ttu-id="42dd8-145">เปิดใช้งานการแจ้งเตือนการเช็คอินของลูกค้าในการขายหน้าร้าน (POS)</span><span class="sxs-lookup"><span data-stu-id="42dd8-145">Enable customer check-in notifications in point of sale (POS)</span></span>](enable-customer-check-in.md)
