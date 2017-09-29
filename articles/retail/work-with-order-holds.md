---
title: "การระงับใบสั่ง"
description: "หัวข้อนี้อธิบายการระงับใบสั่งโดยใช้ Dynamics 365 for Retail"
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 79132
ms.assetid: 7c00dc35-73e5-400a-8587-22f37ddfc0e0
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 14dab07075a3f042e0095b912e51768ccb086f0e
ms.contentlocale: th-th
ms.lasthandoff: 07/18/2017

---

# <a name="order-holds"></a><span data-ttu-id="33427-103">การระงับใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="33427-103">Order holds</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="33427-104">หัวข้อนี้อธิบายการระงับใบสั่งโดยใช้ Dynamics 365 for Retail</span><span class="sxs-lookup"><span data-stu-id="33427-104">This topic describes holds on orders using Dynamics 365 for Retail.</span></span>

<span data-ttu-id="33427-105">ใบสั่งสามารถถูกระงับไว้เพื่อเหตุผลต่าง ๆ</span><span class="sxs-lookup"><span data-stu-id="33427-105">An order can be put on hold for various reasons.</span></span> <span data-ttu-id="33427-106">ตัวอย่างเช่น คุณอาจระงับใบสั่งจนกระทั่งที่อยู่ของลูกค้าหรือวิธีการชำระเงินสามารถถูกตรวจสอบได้ หรือผู้จัดการสามารถตรวจทานวงเงินสินเชื่อของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="33427-106">For example, you might put an order on hold until the customer address or payment method can be verified, or until a manager can review the customer’s credit limit.</span></span> <span data-ttu-id="33427-107">ในระหว่างกระบวนการขาย มีหลายครั้งที่ใบสั่งขายต้องถูกระงับ</span><span class="sxs-lookup"><span data-stu-id="33427-107">During the sales process, there are times when sales orders must be put on hold.</span></span> <span data-ttu-id="33427-108">ตัวอย่างเช่น ใบสั่งขายอาจถูกระงับเนื่องจากปัญหาเกี่ยวกับการชำระเงินของลูกค้า เนื่องจากการฉ้อโกงที่ต้องสงสัย หรือเนื่อง จากผู้จัดการต้องตรวจทานใบสั่ง</span><span class="sxs-lookup"><span data-stu-id="33427-108">For example, a sales order might be put on hold because of issues with a customer payment, because of suspected fraud, or because a manager must review the order.</span></span> <span data-ttu-id="33427-109">เมื่อใบสั่งขายถูกระงับ รหัสการระงับใบสั่งถูกกำหนดให้กับใบสั่งขายเพื่อระบุเหตุผลสำหรับการระงับ</span><span class="sxs-lookup"><span data-stu-id="33427-109">When a sales order is put on hold, an order hold code is assigned to the sales order to indicate the reason for the hold.</span></span> <span data-ttu-id="33427-110">รหัสการระงับใบสั่งขายถูกจัดโครงแบบที่ **การขายและการตลาด** &gt; **ตั้งค่า** &gt; **ใบสั่งขาย** &gt; **รหัสระงับใบสั่ง**</span><span class="sxs-lookup"><span data-stu-id="33427-110">Sales order hold codes are configured at **Sales and marketing** &gt; **Setup** &gt; **Sales orders** &gt; **Order holds codes**.</span></span> <span data-ttu-id="33427-111">ใบสั่งขายสามารถถูกระงับด้วยตนเองในเวลาของการสร้างใบสั่ง หรือในภายหลัง</span><span class="sxs-lookup"><span data-stu-id="33427-111">A sales order can be put on hold manually at the time of order creation or later.</span></span> <span data-ttu-id="33427-112">นอกจากนี้ ใบสั่งสามารถถูกระงับโดยอัตโนมัติ ตามกฎการฉ้อโกง</span><span class="sxs-lookup"><span data-stu-id="33427-112">Additionally, an order can be put on hold automatically, based on fraud rules.</span></span> <span data-ttu-id="33427-113">ขณะที่ใบสั่งขายถูกระงับ คุณอาจต้องอัพเดตข้อมูลเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="33427-113">While a sales order is on hold, you might have to update it with more information.</span></span> <span data-ttu-id="33427-114">โดยมีอีกทางหนึ่ง คุณอาจต้องการเช็คใบสั่งขายในขณะที่คุณทำงานนั้นต่อ</span><span class="sxs-lookup"><span data-stu-id="33427-114">Alternatively, you might want to check out the sales order as you continue to work on it.</span></span> <span data-ttu-id="33427-115">คุณสามารถเช็คใบสั่งขาย เช็คกลับเข้าไป และแม้แต่แทนที่การเช็คเอาท์ของผู้ใช้รายอื่นโดยการใช้ใบสั่งระงับเวิร์กเบนช์ (**การขายปลีก** &gt; **ลูกค้า** &gt; **ระงับใบสั่ง**)</span><span class="sxs-lookup"><span data-stu-id="33427-115">You can check out a sales order, check it back in, and even override the checkout of another user by using the order hold workbench (**Retail** &gt; **Customers** &gt; **Order holds**).</span></span> <span data-ttu-id="33427-116">เมื่อใบสั่งพร้อมดำเนินการให้เสร็จสมบูรณ์ คุณต้องลบการระงับก่อนจึงจะสามารถดำเนินกระบวนการใบสั่ง </span><span class="sxs-lookup"><span data-stu-id="33427-116">When an order is ready to be completed, you must remove the hold before you can complete the order process.</span></span>




