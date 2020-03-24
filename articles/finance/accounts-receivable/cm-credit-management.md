---
title: การจัดการเครดิตของลูกค้า
description: การจัดการเครดิตของลูกค้าช่วยให้คุณสามารถจัดการวงเงินสินเชื่อและควบคุมกระบวนการผลิตของใบสั่งขาย โดยใช้กระบวนการลงรายการบัญชีตามกฎเครดิตที่คุณสร้างขึ้น
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1e7d3325587d7cfc876e8f8c7b9207d44046ccd4
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124288"
---
# <a name="customer-credit-management-overview"></a><span data-ttu-id="4be08-103">ภาพรวมการจัดการเครดิตของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="4be08-103">Customer credit management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4be08-104">การจัดการเครดิตของลูกค้าช่วยให้คุณสามารถจัดการวงเงินสินเชื่อและควบคุมกระบวนการผลิตของใบสั่งขาย โดยใช้กระบวนการลงรายการบัญชีตามกฎเครดิตที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="4be08-104">Customer credit management allows you to manage credit limits and control the flow of sales orders through the posting process based on credit rules that you create.</span></span> 

<span data-ttu-id="4be08-105">กระบวนการในการใช้การจัดการเครดิตอาจประกอบด้วยขั้นตอนต่อไปนี้บางขั้นตอนหรือทั้งหมด:</span><span class="sxs-lookup"><span data-stu-id="4be08-105">The process for using credit management can include some or all of the following steps:</span></span>
- <span data-ttu-id="4be08-106">ปรับปรุงลูกค้าด้วยแอททริบิวต์เครดิตที่ให้ข้อมูลเพิ่มเติมเกี่ยวกับความน่าเชื่อถือของผู้ถือบัตรเครดิต</span><span class="sxs-lookup"><span data-stu-id="4be08-106">Update customers with credit attributes that provide additional information about their credit worthiness</span></span> 
- <span data-ttu-id="4be08-107">สร้างวงเงินสินเชื่อสำหรับลูกค้าโดยใช้การปรับปรุงวงเงินสินเชื่อ</span><span class="sxs-lookup"><span data-stu-id="4be08-107">Create credit limits for customers using credit limit adjustments</span></span>
- <span data-ttu-id="4be08-108">สร้างวงเงินสินเชื่อชั่วคราวสำหรับลูกค้าโดยใช้การปรับปรุงวงเงินสินเชื่อ เมื่อคุณต้องการเพิ่มหรือลดวงเงินสินเชื่อตามความต้องการของธุรกิจชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="4be08-108">Create temporary credit limits for customers using credit limit adjustments when you want to increase or decrease their credit limit temporarily based on business needs</span></span>
- <span data-ttu-id="4be08-109">เพิ่มข้อมูลเพิ่มเติมที่อาจส่งผลกระทบต่อวงเงินสินเชื่อ เช่น การประกันภัยและการค้ำประกัน</span><span class="sxs-lookup"><span data-stu-id="4be08-109">Add additional information that can affect the credit limit such as insurance and guarantees</span></span>
- <span data-ttu-id="4be08-110">สร้างกลุ่มเครดิตของลูกค้าที่เชื่อมโยงกับลูกค้าด้วยกัน เพื่อให้สามารถใช้วงเงินสินเชื่อเดียวกันได้</span><span class="sxs-lookup"><span data-stu-id="4be08-110">Create customer credit groups that link customers together so they can share a single credit limit</span></span>
- <span data-ttu-id="4be08-111">กำหนดคะแนนความเสี่ยงให้กับลูกค้า แล้วใช้คะแนนเหล่านั้นเพื่อสร้างวงเงินสินเชื่อสำหรับลูกค้าโดยอัตโนมัติ โดยใช้การปรับปรุงวงเงินสินเชื่อ</span><span class="sxs-lookup"><span data-stu-id="4be08-111">Assign risk scores to customers and then use those scores to automatically generate credit limits for customers using credit limit adjustments</span></span>
- <span data-ttu-id="4be08-112">สร้างกฎการบล็อคที่จะทำการระงับใบสั่งระหว่างกระบวนการลงรายการบัญชีอย่างน้อยหนึ่งรายการตามปัจจัยต่าง ๆ เช่น ความเสี่ยง เงื่อนไขการชำระเงิน วงเงินสินเชื่อ ยอดเงินที่พ้นกำหนดชำระ และเปอร์เซ็นต์ของวงเงินสินเชื่อที่ใช้</span><span class="sxs-lookup"><span data-stu-id="4be08-112">Create blocking rules that will place an order on hold during one or more posting processes based on factors such as risk, payment terms, credit limits, overdue amounts, and percentage of credit limit used</span></span>
- <span data-ttu-id="4be08-113">จัดการรายการของใบสั่งขายที่ระงับ ตรวจสอบเหตุผลสำหรับการระงับ และลดปัญหา</span><span class="sxs-lookup"><span data-stu-id="4be08-113">Manage a list of sales orders that are on hold, review the reasons for the hold, and mitigate the issues</span></span>
- <span data-ttu-id="4be08-114">นำใบสั่งขายออกใช้ และอนุญาตให้ดำเนินการต่อโดยใช้กระบวนการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="4be08-114">Release sales orders and allow it to continue through the posting process</span></span>
- <span data-ttu-id="4be08-115">ตั้งค่าลำดับงานเพื่อจัดการการอนุมัติการเปลี่ยนแปลงวงเงินสินเชื่อ และการนำใบสั่งขายออกใช้</span><span class="sxs-lookup"><span data-stu-id="4be08-115">Set up workflow to manage the approval of credit limit changes and sales order releases</span></span>


<a name="additional-resources"></a><span data-ttu-id="4be08-116">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="4be08-116">Additional resources</span></span>
--------
[<span data-ttu-id="4be08-117">การตั้งค่าพารามิเตอร์การจัดการเครดิตของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="4be08-117">Customer credit management parameters setup</span></span>](./cm-credit-mgmt-setup.md)

[<span data-ttu-id="4be08-118">ข้อมูลการตั้งค่าการจัดการเครดิตของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="4be08-118">Customer credit management setup information</span></span>](./cm-setup-information.md)

[<span data-ttu-id="4be08-119">เพิ่มข้อมูลการตั้งค่าการจัดการเครดิตสำหรับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="4be08-119">Add credit management information for a customer</span></span>](./cm-add-credit-mgmt-information-customer.md)

[<span data-ttu-id="4be08-120">กลุ่มสินเชื่อลูกค้า</span><span class="sxs-lookup"><span data-stu-id="4be08-120">Customer credit groups</span></span>](./cm-customer-credit-groups.md)

[<span data-ttu-id="4be08-121">การปรับปรุงวงเงินเครดิตลูกค้า</span><span class="sxs-lookup"><span data-stu-id="4be08-121">Customer credit limit adjustments</span></span>](./cm-credit-limit-adjustments.md)

[<span data-ttu-id="4be08-122">การระงับเครดิตสำหรับใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="4be08-122">Credit holds for sales orders</span></span>](./cm-sales-order-credit-holds.md)

[<span data-ttu-id="4be08-123">งานประจำงวดการจัดการเครดิตของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="4be08-123">Customer credit management periodic tasks</span></span>](./cm-periodic-tasks.md)


