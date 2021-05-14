---
title: ใบสำคัญไม่ถูกสร้าง
description: หัวข้อนี้มีข้อมูลการแก้ไขปัญหาที่สามารถช่วยเมื่อควรสร้างใบสำคัญแต่ไม่ถูกสร้าง
author: qire
manager: beya
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: eafc9110ec58be5083569188d59b67a62e86c85d
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947718"
---
# <a name="voucher-isnt-generated"></a><span data-ttu-id="85f9a-103">ใบสำคัญไม่ถูกสร้าง</span><span class="sxs-lookup"><span data-stu-id="85f9a-103">Voucher isn't generated</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="85f9a-104">ถ้าใบสำคัญควรจะสร้าง แต่หน้า **ธุรกรรมใบสำคัญ** ไม่แสดงใบสำคัญใด ๆ ให้ปฏิบัติตามขั้นตอนในส่วนต่อไปนี้ตามที่ต้องการเพื่อแก้ไขปัญหานี้</span><span class="sxs-lookup"><span data-stu-id="85f9a-104">If a voucher should be generated, but the **Voucher transactions** page doesn't show any vouchers, follow the steps in the following sections as required to troubleshoot this issue.</span></span>

<span data-ttu-id="85f9a-105">[![หน้าธุรกรรมใบสำคัญที่ไม่มีใบสำคัญ](./media/voucher-not-generated-Picture1.png)](./media/voucher-not-generated-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="85f9a-105">[![Voucher transactions page that has no vouchers](./media/voucher-not-generated-Picture1.png)](./media/voucher-not-generated-Picture1.png)</span></span>

## <a name="check-the-tax-applicability"></a><span data-ttu-id="85f9a-106">ตรวจสอบการใช้งานภาษี</span><span class="sxs-lookup"><span data-stu-id="85f9a-106">Check the tax applicability</span></span>

1. <span data-ttu-id="85f9a-107">ไปที่ **ภาษี** \> **งานประจำงวด** \> **รายการสมุดรายวันของบัญชีแยกประเภทย่อยที่ยังไม่ได้โอนย้าย**</span><span class="sxs-lookup"><span data-stu-id="85f9a-107">Go to **Tax** \> **Periodic tasks** \> **Subledger journal entries not yet transferred**.</span></span>
2. <span data-ttu-id="85f9a-108">ถ้ามีเรกคอร์ดสมุดรายวัน ให้เลือกเรกคอร์ดนั้น แล้วเลือก **โอนย้ายทันที**</span><span class="sxs-lookup"><span data-stu-id="85f9a-108">If there is a journal record, select it, and then select **Transfer now**.</span></span>

    <span data-ttu-id="85f9a-109">[![ปุ่ม โอนย้ายทันที บนหน้ารายการสมุดรายวันของบัญชีแยกประเภทย่อยที่ยังไม่ได้โอนย้าย](./media/voucher-not-generated-Picture2.png)](./media/voucher-not-generated-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="85f9a-109">[![Transfer now button on the Subledger journal entries not yet transferred page](./media/voucher-not-generated-Picture2.png)](./media/voucher-not-generated-Picture2.png)</span></span>

3. <span data-ttu-id="85f9a-110">เปิด **หน้าธุรกรรมใบสำคัญ** อีกครั้ง เพื่อดูว่ามีการสร้างใบสำคัญหรือไม่</span><span class="sxs-lookup"><span data-stu-id="85f9a-110">Open the **Voucher transactions** page again to see whether the voucher was generated.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="85f9a-111">ระบุว่ามีการเลือกเองอยู่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="85f9a-111">Determine whether customization exists</span></span>

<span data-ttu-id="85f9a-112">หากคุณได้เสร็จสิ้นขั้นตอนในส่วนก่อนหน้านี้แต่ไม่พบปัญหา ให้ระบุว่ามีการเลือกเองอยู่หรือไม่</span><span class="sxs-lookup"><span data-stu-id="85f9a-112">If you've completed the steps in the previous section but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="85f9a-113">ถ้าไม่มีการเลือกเองอยู่ ให้สร้างคำขอบริการของ Microsoft เพื่อขอความช่วยเหลือเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="85f9a-113">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
