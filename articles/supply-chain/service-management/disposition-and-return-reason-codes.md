---
title: ภาพรวมของการส่งคืนของลูกค้า
description: สร้างและใช้รหัสเหตุผลการส่งคืนและรหัสการโอนการครอบครอง เพื่อสนับสนุนกระบวนการสำหรับการส่งคืนผลิตภัณฑ์
author: ShylaThompson
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReturnTableListPage, ReturnReasonCodeLookup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2c352c91ee9a6ae97d8cab12abb8a91e77a3d2b3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5247393"
---
# <a name="customer-returns-overview"></a><span data-ttu-id="3a25c-103">ภาพรวมของการส่งคืนของลูกค้า</span><span class="sxs-lookup"><span data-stu-id="3a25c-103">Customer returns overview</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="3a25c-104">สร้างและใช้รหัสเหตุผลการส่งคืนและรหัสการโอนการครอบครอง เพื่อสนับสนุนกระบวนการสำหรับการส่งคืนผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="3a25c-104">Create and use return reason codes and disposition codes to support the process for returning products.</span></span>

<span data-ttu-id="3a25c-105">ใช้รหัสเหตุผลการส่งคืนใช้เพื่ออธิบายเหตุผลที่ลูกค้าต้องการส่งคืนสินค้า </span><span class="sxs-lookup"><span data-stu-id="3a25c-105">Use a return reason code to describe the reason that the customer wants to return an item.</span></span> <span data-ttu-id="3a25c-106">คุณสามารถกำหนดรหัสเหตุผลในแบบฟอร์ม **สร้างใบสั่งส่งคืนสินค้า** ได้</span><span class="sxs-lookup"><span data-stu-id="3a25c-106">You can assign a reason code in the **Create return orders** form.</span></span>

<span data-ttu-id="3a25c-107">กำหนดรหัสการโอนการครอบครองเมื่อรับสินค้า หรือในระหว่างการตรวจสอบทางกายภาพของสินค้าที่ส่งคืน </span><span class="sxs-lookup"><span data-stu-id="3a25c-107">Assign a disposition code when an item is received or during the physical inspection of a returned item.</span></span> <span data-ttu-id="3a25c-108">คุณสามารถใช้รหัสการโอนการครอบครองเพื่ออธิบายเงื่อนไขของสินค้า </span><span class="sxs-lookup"><span data-stu-id="3a25c-108">You can use disposition codes to describe the condition of the item.</span></span> <span data-ttu-id="3a25c-109">คุณยังสามารถใช้รหัสการโอนการครอบครองเพื่อบ่งชี้ว่าการดำเนินการเพิ่มเติมจำเป็นสำหรับธุรกรรมหรือไม่ </span><span class="sxs-lookup"><span data-stu-id="3a25c-109">You can also use disposition codes to indicate whether additional action is required for the transaction.</span></span> <span data-ttu-id="3a25c-110">ตัวอย่างเช่น สร้างรหัสการโอนการครอบครองสำหรับการดำเนินการต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="3a25c-110">For example, create disposition codes for the following actions:</span></span>

  - <span data-ttu-id="3a25c-111">ทำสินค้าที่ส่งคืนเป็นของเสียและระบุสินค้าทดแทนให้กับลูกค้า</span><span class="sxs-lookup"><span data-stu-id="3a25c-111">Scrap the returned item and provide a replacement item to the customer.</span></span>

  - <span data-ttu-id="3a25c-112">ส่งคืนสินค้าไปยังสินค้าคงคลัง และเครดิตลูกค้าสำหรับต้นทุนของสินค้า</span><span class="sxs-lookup"><span data-stu-id="3a25c-112">Return the item to inventory and credit the customer for the cost of the item.</span></span>

  - <span data-ttu-id="3a25c-113">ซ่อมสินค้าและส่งกลับให้ลูกค้า</span><span class="sxs-lookup"><span data-stu-id="3a25c-113">Repair the item and return it to the customer.</span></span>

## <a name="see-also"></a><span data-ttu-id="3a25c-114">ดูเพิ่มเติมที่</span><span class="sxs-lookup"><span data-stu-id="3a25c-114">See also</span></span>

[<span data-ttu-id="3a25c-115">การตั้งค่ารหัสเหตุผลการส่งคืน</span><span class="sxs-lookup"><span data-stu-id="3a25c-115">Set up return reason codes</span></span>](set-up-return-reason-code.md)

[<span data-ttu-id="3a25c-116">ตั้งค่ารหัสการโอนการครอบครอง</span><span class="sxs-lookup"><span data-stu-id="3a25c-116">Set up disposition codes</span></span>](set-up-disposition-codes.md)




  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]