---
title: การจัดการเครดิตของลูกค้า
description: ''
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
ms.openlocfilehash: 11da8b7fb59bc8f3e2568ada27db753cc815b9c2
ms.sourcegitcommit: 6a70f9ac296158edd065d52a12703b3ce85ce5ee
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/03/2020
ms.locfileid: "3015413"
---
# <a name="customer-credit-management-overview"></a><span data-ttu-id="8f00b-102">ภาพรวมการจัดการเครดิตของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="8f00b-102">Customer credit management overview</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="8f00b-103">การจัดการเครดิตของลูกค้าช่วยให้คุณสามารถจัดการวงเงินสินเชื่อและควบคุมกระบวนการผลิตของใบสั่งขาย โดยใช้กระบวนการลงรายการบัญชีตามกฎเครดิตที่คุณสร้างขึ้น</span><span class="sxs-lookup"><span data-stu-id="8f00b-103">Customer credit management allows you to manage credit limits and control the flow of sales orders through the posting process based on credit rules that you create.</span></span> 

<span data-ttu-id="8f00b-104">กระบวนการในการใช้การจัดการเครดิตอาจประกอบด้วยขั้นตอนต่อไปนี้บางขั้นตอนหรือทั้งหมด:</span><span class="sxs-lookup"><span data-stu-id="8f00b-104">The process for using credit management can include some or all of the following steps:</span></span>
- <span data-ttu-id="8f00b-105">ปรับปรุงลูกค้าด้วยแอททริบิวต์เครดิตที่ให้ข้อมูลเพิ่มเติมเกี่ยวกับความน่าเชื่อถือของผู้ถือบัตรเครดิต</span><span class="sxs-lookup"><span data-stu-id="8f00b-105">Update customers with credit attributes that provide additional information about their credit worthiness</span></span> 
- <span data-ttu-id="8f00b-106">สร้างวงเงินสินเชื่อสำหรับลูกค้าโดยใช้การปรับปรุงวงเงินสินเชื่อ</span><span class="sxs-lookup"><span data-stu-id="8f00b-106">Create credit limits for customers using credit limit adjustments</span></span>
- <span data-ttu-id="8f00b-107">สร้างวงเงินสินเชื่อชั่วคราวสำหรับลูกค้าโดยใช้การปรับปรุงวงเงินสินเชื่อ เมื่อคุณต้องการเพิ่มหรือลดวงเงินสินเชื่อตามความต้องการของธุรกิจชั่วคราว</span><span class="sxs-lookup"><span data-stu-id="8f00b-107">Create temporary credit limits for customers using credit limit adjustments when you want to increase or decrease their credit limit temporarily based on business needs</span></span>
- <span data-ttu-id="8f00b-108">เพิ่มข้อมูลเพิ่มเติมที่อาจส่งผลกระทบต่อวงเงินสินเชื่อ เช่น การประกันภัยและการค้ำประกัน</span><span class="sxs-lookup"><span data-stu-id="8f00b-108">Add additional information that can affect the credit limit such as insurance and guarantees</span></span>
- <span data-ttu-id="8f00b-109">สร้างกลุ่มเครดิตของลูกค้าที่เชื่อมโยงกับลูกค้าด้วยกัน เพื่อให้สามารถใช้วงเงินสินเชื่อเดียวกันได้</span><span class="sxs-lookup"><span data-stu-id="8f00b-109">Create customer credit groups that link customers together so they can share a single credit limit</span></span>
- <span data-ttu-id="8f00b-110">กำหนดคะแนนความเสี่ยงให้กับลูกค้า แล้วใช้คะแนนเหล่านั้นเพื่อสร้างวงเงินสินเชื่อสำหรับลูกค้าโดยอัตโนมัติ โดยใช้การปรับปรุงวงเงินสินเชื่อ</span><span class="sxs-lookup"><span data-stu-id="8f00b-110">Assign risk scores to customers and then use those scores to automatically generate credit limits for customers using credit limit adjustments</span></span>
- <span data-ttu-id="8f00b-111">สร้างกฎการบล็อคที่จะทำการระงับใบสั่งระหว่างกระบวนการลงรายการบัญชีอย่างน้อยหนึ่งรายการตามปัจจัยต่าง ๆ เช่น ความเสี่ยง เงื่อนไขการชำระเงิน วงเงินสินเชื่อ ยอดเงินที่พ้นกำหนดชำระ และเปอร์เซ็นต์ของวงเงินสินเชื่อที่ใช้</span><span class="sxs-lookup"><span data-stu-id="8f00b-111">Create blocking rules that will place an order on hold during one or more posting processes based on factors such as risk, payment terms, credit limits, overdue amounts, and percentage of credit limit used</span></span>
- <span data-ttu-id="8f00b-112">จัดการรายการของใบสั่งขายที่ระงับ ตรวจสอบเหตุผลสำหรับการระงับ และลดปัญหา</span><span class="sxs-lookup"><span data-stu-id="8f00b-112">Manage a list of sales orders that are on hold, review the reasons for the hold, and mitigate the issues</span></span>
- <span data-ttu-id="8f00b-113">นำใบสั่งขายออกใช้ และอนุญาตให้ดำเนินการต่อโดยใช้กระบวนการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="8f00b-113">Release sales orders and allow it to continue through the posting process</span></span>
- <span data-ttu-id="8f00b-114">ตั้งค่าลำดับงานเพื่อจัดการการอนุมัติการเปลี่ยนแปลงวงเงินสินเชื่อ และการนำใบสั่งขายออกใช้</span><span class="sxs-lookup"><span data-stu-id="8f00b-114">Set up workflow to manage the approval of credit limit changes and sales order releases</span></span>


<a name="additional-resources"></a><span data-ttu-id="8f00b-115">แหล่งข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="8f00b-115">Additional resources</span></span>
--------
[<span data-ttu-id="8f00b-116">การตั้งค่าพารามิเตอร์การจัดการเครดิตของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="8f00b-116">Customer credit management parameters setup</span></span>](./cm-credit-mgmt-setup.md)

[<span data-ttu-id="8f00b-117">ข้อมูลการตั้งค่าการจัดการเครดิตของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="8f00b-117">Customer credit management setup information</span></span>](./cm-setup-information.md)

[<span data-ttu-id="8f00b-118">เพิ่มข้อมูลการตั้งค่าการจัดการเครดิตสำหรับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="8f00b-118">Add credit management information for a customer</span></span>](./cm-add-credit-mgmt-information-customer.md)

[<span data-ttu-id="8f00b-119">กลุ่มสินเชื่อลูกค้า</span><span class="sxs-lookup"><span data-stu-id="8f00b-119">Customer credit groups</span></span>](./cm-customer-credit-groups.md)

[<span data-ttu-id="8f00b-120">การปรับปรุงวงเงินเครดิตลูกค้า</span><span class="sxs-lookup"><span data-stu-id="8f00b-120">Customer credit limit adjustments</span></span>](./cm-credit-limit-adjustments.md)

[<span data-ttu-id="8f00b-121">การระงับเครดิตสำหรับใบสั่งขาย</span><span class="sxs-lookup"><span data-stu-id="8f00b-121">Credit holds for sales orders</span></span>](./cm-sales-order-credit-holds.md)

[<span data-ttu-id="8f00b-122">งานประจำงวดการจัดการเครดิตของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="8f00b-122">Customer credit management periodic tasks</span></span>](./cm-periodic-tasks.md)


