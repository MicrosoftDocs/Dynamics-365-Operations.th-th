---
title: การปรับปรุงให้มีการจัดการสินค้าที่มีการติดตามแบบชุดงาน
description: หัวข้อนี้อธิบายถึงการปรับปรุงที่ดำเนินการกับการจัดการชุดงานของสินค้าที่มีการติดตามแบบชุดงานระหว่างกระบวนการลงรายการบัญชีใบแจ้งยอดการขายปลีก
author: josaw1
manager: AnnBe
ms.date: 05/28/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: 10
ms.openlocfilehash: 4456fc3d5bc4547fa8211642b11ca6df455fa187
ms.sourcegitcommit: aec1dcd44274e9b8d0770836598fde5533b7b569
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/03/2019
ms.locfileid: "1617400"
---
# <a name="improved-handling-of-batch-tracked-items"></a><span data-ttu-id="96dfd-103">การปรับปรุงให้มีการจัดการสินค้าที่มีการติดตามแบบชุดงาน</span><span class="sxs-lookup"><span data-stu-id="96dfd-103">Improved handling of batch-tracked items</span></span>

<span data-ttu-id="96dfd-104">ในการขายหน้าร้าน (POS) ของ Microsoft Dynamics 365 for Retail ไม่สามารถบันทึกหมายเลขชุดงานสำหรับสินค้าที่มีการติดตามแบบชุดงานในเวลาที่ขาย</span><span class="sxs-lookup"><span data-stu-id="96dfd-104">In Microsoft Dynamics 365 for Retail Point of Sale (POS), batch numbers can't be captured for batch-tracked items at the time of sale.</span></span> <span data-ttu-id="96dfd-105">อย่างไรก็ตาม สำหรับการตั้งค่าคอนฟิกเฉพาะ เมื่อมีการลงรายการบัญชียอดขายในศูนย์ควบคุมผ่านทางใบสั่งของลูกค้าหรือการลงรายการบัญชีใบแจ้งยอด ระบบ Microsoft Dynamics คาดว่าจะมีหมายเลขชุดงานที่ถูกต้องของสินค้าที่มีการติดตามแบบชุดงาน และระบบจะใช้หมายเลขดังกล่าวในกระบวนการออกใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="96dfd-105">However, for specific configurations, when sales are posted in the headquarters through customer orders or statement posting, the Microsoft Dynamics system expects that valid batch numbers for batch-tracked items exist, and that they will be used during the invoicing process.</span></span>

<span data-ttu-id="96dfd-106">หากมีหมายเลขชุดงานที่ถูกต้องของผลิตภัณฑ์ กระบวนการออกใบแจ้งหนี้ใบสั่งของลูกค้าและกระบวนการออกใบแจ้งหนี้ใบสั่งขายจากการลงรายการบัญชีใบแจ้งยอดจะใช้หมายเลขดังกล่าว</span><span class="sxs-lookup"><span data-stu-id="96dfd-106">If valid batch numbers are available for products, the customer order invoicing process and the sales order invoicing process from statement posting use them.</span></span> <span data-ttu-id="96dfd-107">ไม่เช่นนั้น กระบวนการออกใบแจ้งหนี้ใบสั่งของลูกค้าจะไม่สามารถลงรายการบัญชี และผู้ใช้ POS จะได้รับข้อความแสดงข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="96dfd-107">Otherwise, the customer order invoicing process can't post, and the POS user receives an error message.</span></span> <span data-ttu-id="96dfd-108">จากนั้นการลงรายการบัญชีใบแจ้งยอดจะเข้าสู่สถานะข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="96dfd-108">Statement posting then goes into an error state.</span></span> <span data-ttu-id="96dfd-109">สถานะข้อผิดพลาดนี้จะเกิดขึ้นแม้เมื่อมีการเปิดสินค้าคงคลังติดลบสำหรับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="96dfd-109">This error state occurs even when negative inventory has been turned on for the products.</span></span>

<span data-ttu-id="96dfd-110">การปรับปรุงที่ดำเนินการใน Microsoft Dynamics for Retail รุ่น 10.0.4 และที่ใหม่กว่าจะช่วยรับประกันว่า เมื่อเปิดสินค้าคงคลังติดลบสำหรับสินค้าที่มีการติดตามแบบชุดงาน การออกใบแจ้งหนี้ใบสั่งของลูกค้าและการออกใบแจ้งหนี้ใบสั่งขายผ่านการลงรายการบัญชีใบแจ้งยอดจะไม่ถูกบล็อคสำหรับสินค้าเหล่านั้นหากสินค้าคงคลังเป็น 0 (ศูนย์) หรือไม่มีหมายเลขชุดงาน</span><span class="sxs-lookup"><span data-stu-id="96dfd-110">Improvements that have been made in Microsoft Dynamics for Retail version 10.0.4 and later help guarantee that, when negative inventory is turned on for batch-tracked items, customer order invoicing and sales order invoicing through statement posting aren't blocked for those items if the inventory is 0 (zero) or a batch number isn't available.</span></span> <span data-ttu-id="96dfd-111">ฟังก์ชันใหม่นี้จะใช้รหัสชุดงานเริ่มต้นกับรายการขายเมื่อไม่มีหมายเลขชุดงาน</span><span class="sxs-lookup"><span data-stu-id="96dfd-111">The new functionality uses a default batch ID for the sales lines when batch numbers aren't available.</span></span>

<span data-ttu-id="96dfd-112">หากต้องการกำหนดรหัสชุดงานเริ่มต้นที่ใช้กับใบสั่งของลูกค้า ในหน้า **พารามิเตอร์การขายปลีก** บนแท็บ **ใบสั่งของลูกค้า** บนแท็บด่วน **ใบสั่ง** ให้ตั้งค่าฟิลด์ **รหัสชุดงานเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="96dfd-112">To define the default batch ID that is used for customer orders, on the **Retail parameters** page, on the **Customer orders** tab, on the **Order** FastTab, set the **Default batch id** field.</span></span>

<span data-ttu-id="96dfd-113">หากต้องการกำหนดรหัสชุดงานเริ่มต้นที่ใช้กับการออกใบแจ้งหนี้ใบสั่งขายผ่านการลงรายการบัญชีใบแจ้งยอด ในหน้า **พารามิเตอร์การขายปลีก** บนแท็บ **การลงรายการบัญชี** บนแท็บด่วน **การอัพเดตสินค้าคงคลัง** ให้ตั้งค่าฟิลด์ **รหัสชุดงานเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="96dfd-113">To define the default batch ID that is used for sales order invoicing through statement posting, on the **Retail parameters** page, on the **Posting** tab, on the **Inventory update** FastTab, set the **Default batch id** field.</span></span>

> [!NOTE]
> <span data-ttu-id="96dfd-114">ฟังก์ชันนี้สามารถใช้ได้เฉพาะเมื่อมีการเปิดการจัดการคลังสินค้าขั้นสูงสำหรับคลังสินค้าและสินค้าของร้านค้าเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="96dfd-114">This functionality is available only when advanced warehousing is turned on for the specific store warehouse and items.</span></span> <span data-ttu-id="96dfd-115">ในรุ่นถัดไป ฟังก์ชันนี้จะใช้รองรับสถานการณ์ที่ไม่ได้ใช้การจัดการคลังสินค้าขั้นสูงด้วย</span><span class="sxs-lookup"><span data-stu-id="96dfd-115">In a later release, the functionality will also be supported for scenarios where advanced warehouse management isn't used.</span></span>
