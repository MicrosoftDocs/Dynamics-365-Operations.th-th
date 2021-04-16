---
title: FAQ เกี่ยวกับใบสำคัญหนึ่งใบ
description: หัวข้อนี้ตอบคำถามที่ถามบ่อยเกี่ยวกับฟังก์ชันใบสำคัญหนึ่งใบเท่านั้น ใบสำคัญหนึ่งใบสำหรับสมุดรายวันทางการเงิน (สมุดรายวันทั่วไป สมุดรายวันสินทรัพย์ถาวร สมุดรายวันการชำระเงินของผู้จัดจำหน่าย และอื่นๆ) ช่วยให้คุณสามารถป้อนธุรกรรมบัญชีแยกประเภทย่อยต่างๆ ได้ในบริบทของใบสำคัญใบเดียว
author: kweekley
ms.date: 11/05/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerParameters, AssetProposalDepreciation
audience: Application User
ms.reviewer: roschlom
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-03-16
ms.dyn365.ops.version: 8.0.2
ms.openlocfilehash: 1a2c677f853e4d524ad5fc91ea9ee34315608e24
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815559"
---
# <a name="one-voucher-faq"></a><span data-ttu-id="4573b-104">FAQ เกี่ยวกับใบสำคัญหนึ่งใบ</span><span class="sxs-lookup"><span data-stu-id="4573b-104">One voucher FAQ</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4573b-105">หัวข้อนี้ตอบคำถามที่ถามบ่อยเกี่ยวกับฟังก์ชันใบสำคัญหนึ่งใบเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="4573b-105">This topic answers frequently asked questions about the One voucher functionality.</span></span> <span data-ttu-id="4573b-106">ใบสำคัญหนึ่งใบจากสมุดรายวันทางการเงินช่วยให้คุณสามารถป้อนธุรกรรมของบัญชีแยกประเภทย่อยหลายธุรกรรมในบริบทของใบเดียว</span><span class="sxs-lookup"><span data-stu-id="4573b-106">One voucher for financial journals lets you enter multiple subledger transactions in the context of a single voucher.</span></span> <span data-ttu-id="4573b-107">สมุดรายวันที่คุณสามารถรวมในใบแจ้งนี้ อาจเป็นสมุดรายวันทั่วไป สมุดรายวันสินทรัพย์ถาวร และสมุดรายวันการจ่ายเงินให้แก่ผู้ขอซื้อ ในสมุดรายวันอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="4573b-107">The journals that you can include in that voucher can be general journals, fixed asset journals, and vendor payment journals, among others.</span></span>

## <a name="when-will-the-one-voucher-functionality-be-deprecated"></a><span data-ttu-id="4573b-108">ไม่สนับสนุนฟังก์ชันใบสำคัญหนึ่งใบเมื่อใด</span><span class="sxs-lookup"><span data-stu-id="4573b-108">When will the One voucher functionality be deprecated?</span></span>

<span data-ttu-id="4573b-109">ถึงแม้ว่า Microsoft ไม่สามารถให้การประเมินที่ถูกต้องเกี่ยวกับว่าฟังก์ชันใบสำคัญหนึ่งใบจะไม่สนับสนุน แต่อาจมีการเลิกใช้อย่างน้อยสองปีก่อนที่จะเลิกใช้</span><span class="sxs-lookup"><span data-stu-id="4573b-109">Although Microsoft can't provide an accurate estimate about when the One voucher functionality will be deprecated, it will likely be at least two years before the deprecation occurs.</span></span>

<span data-ttu-id="4573b-110">ตามที่ได้พิมพ์ไว้ในคู่มือใบสำคัญหนึ่งใบ สามารถตอบสนองความต้องการทางธุรกิจได้มากมายโดยการใช้ใบสำคัญหนึ่งใบเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="4573b-110">As is noted in the One voucher documentation, numerous business requirements can be met only by using One voucher.</span></span> <span data-ttu-id="4573b-111">Microsoft ต้องตรวจสอบให้แน่ใจว่ายังคงสามารถตอบสนองความต้องการทางธุรกิจที่ระบุทั้งหมดในระบบได้หลังจากที่ไม่สนับสนุนฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="4573b-111">Microsoft must ensure that all the identified business requirements can still be met in the system after the functionality is deprecated.</span></span> <span data-ttu-id="4573b-112">คุณลักษณะใหม่จึงต้องถูกเพิ่มเพื่อเติมช่องว่างของฟังก์ชัน</span><span class="sxs-lookup"><span data-stu-id="4573b-112">Therefore, new features will probably have to be added to fill functional gaps.</span></span>

<span data-ttu-id="4573b-113">หลังจากที่เติมช่องว่างของฟังก์ชันทั้งหมดแล้ว Microsoft จะสื่อสารกับคุณลักษณะนั้นจะไม่สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="4573b-113">After all functional gaps are filled, Microsoft will communicate that the feature will be deprecated.</span></span> <span data-ttu-id="4573b-114">อย่างไรก็ตาม การเลิกใช้จะไม่มีผลบังคับใช้เป็นเวลาหนึ่งปีหลังจากการสื่อสารนั้น</span><span class="sxs-lookup"><span data-stu-id="4573b-114">However, the deprecation won't be effective for least one year after that communication.</span></span>

<span data-ttu-id="4573b-115">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [คู่มือใบสำคัญหนึ่งใบ](one-voucher.md)</span><span class="sxs-lookup"><span data-stu-id="4573b-115">For more information, see the [One voucher documentation](one-voucher.md).</span></span>

## <a name="what-will-the-solution-that-replaces-one-voucher-look-like"></a><span data-ttu-id="4573b-116">โซลูชันที่แทนที่ลักษณะใบสำคัญหนึ่งใบลักษณะอย่างไร</span><span class="sxs-lookup"><span data-stu-id="4573b-116">What will the solution that replaces One voucher look like?</span></span>

<span data-ttu-id="4573b-117">Microsoft ไม่สามารถระบุโซลูชันเฉพาะได้ เนื่องจากช่องว่างของคุณลักษณะแต่ละช่องว่างแตกต่างกันและต้องมีการประเมินตามความต้องการทางธุรกิจ</span><span class="sxs-lookup"><span data-stu-id="4573b-117">Microsoft can't provide a specific solution, because each feature gap is different and must be evaluated based on the business requirements.</span></span> <span data-ttu-id="4573b-118">ช่องว่างของฟังก์ชันบางอย่างจะถูกแทนที่ด้วยคุณลักษณะที่ช่วยตอบสนองความต้องการทางธุรกิจเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="4573b-118">Some functional gaps will likely be replaced with features that help meet specific business requirements.</span></span> <span data-ttu-id="4573b-119">อย่างไรก็ตาม ช่องว่างอื่น ๆ อาจถูกเติมด้วยเพื่อให้สามารถป้อนรายการในสมุดรายวันได้ เนื่องจากเมื่อมีการใช้ใบสำคัญหนึ่งใบ แต่ระบบใช้ระบบเพื่อติดตามรายละเอียดเพิ่มเติมได้ตามที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="4573b-119">However, other gaps might be filled by continuing to allow for entry in a journal, as when One voucher is used, but enhancing the system to track more detail as required.</span></span>

## <a name="where-can-i-track-the-progress-of-the-feature-gaps-being-filled"></a><span data-ttu-id="4573b-120">ฉันจะติดตามความคืบหน้าของช่องว่างของลักษณะการกรอกข้อมูลได้จากที่ใด</span><span class="sxs-lookup"><span data-stu-id="4573b-120">Where can I track the progress of the feature gaps being filled?</span></span>

<span data-ttu-id="4573b-121">เช่นเดียวกับคุณลักษณะใหม่ทั้งหมด ลูกค้าต้องดูแผนที่เผยแพร่และคู่มือ "มีอะไรใหม่หรือที่เปลี่ยนแปลง"</span><span class="sxs-lookup"><span data-stu-id="4573b-121">As for every new feature, customers must watch the Release plan and "What's new or changed" documentation.</span></span> <span data-ttu-id="4573b-122">คุณลักษณะแต่ละอย่างจะถูกเพิ่มเข้าในเอกสารเหล่านี้ และหมายเหตุจะระบุว่าลักษณะการใช้ฟังก์ชันนี้ต้องตรงตามข้อกําหนดทางธุรกิจที่กําหนดไว้ก่อนหน้านี้ว่าฟังก์ชันใบสำคัญหนึ่งใบ</span><span class="sxs-lookup"><span data-stu-id="4573b-122">Each feature will be added to these documents, and a note will indicate that the feature is required to meet a business requirement that previously required the One voucher functionality.</span></span>

## <a name="when-the-deprecation-date-is-identified-where-will-it-be-communicated"></a><span data-ttu-id="4573b-123">เมื่อระบุวันที่การาเลิกใช้ จะมีการสื่อสารเมื่อใด</span><span class="sxs-lookup"><span data-stu-id="4573b-123">When the deprecation date is identified, where will it be communicated?</span></span>

<span data-ttu-id="4573b-124">การเลิกใช้ของใบสําคัญหนึ่งใบเป็นการเปลี่ยนแปลงที่สําคัญที่สําคัญมากซึ่งจะสื่อสารกันอย่างกว้าง</span><span class="sxs-lookup"><span data-stu-id="4573b-124">The deprecation of One voucher is a significant change that will be widely communicated.</span></span> <span data-ttu-id="4573b-125">โดยจะมีการสื่อสารผ่านทางคู่มือผลิตภัณฑ์ การลงรายการบัญชีแบบธนาคาร และประกาศต่างๆ ของการประชุม Microsoft ที่เกี่ยวข้อง ล่วงหน้าด้วยวันที่การเลิกใช้นั้นจะมีผลบังคับ</span><span class="sxs-lookup"><span data-stu-id="4573b-125">It will be communicated through the product documentation, a blog post, and announcements at applicable Microsoft conferences, well in advance of the date when the deprecation takes effect.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]