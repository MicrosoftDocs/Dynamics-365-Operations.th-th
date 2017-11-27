---
title: "แก้ไขส่วนต่างในระหว่างการจับคู่ผลรวมในใบแจ้งหนี้"
description: "คุณสามารถใช้การจับคู่ผลรวมในใบแจ้งหนี้เพื่อรับประกันว่ายอดรวมของใบแจ้งหนี้ไม่เบี่ยงเบนจากยอดเงินที่คาดไว้โดยมากกว่าผลต่างที่ยอมรับได้"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 63413
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 18250a735d0421daa90b923504aeb94b5003a6a7
ms.contentlocale: th-th
ms.lasthandoff: 11/03/2017

---

# <a name="resolve-discrepancies-during-invoice-totals-matching"></a><span data-ttu-id="8e7b4-103">แก้ไขส่วนต่างในระหว่างการจับคู่ผลรวมในใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="8e7b4-103">Resolve discrepancies during invoice totals matching</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="8e7b4-104">ชนิดหนึ่งชนิดของการตรวจสอบการจับคู่ใบแจ้งหนี้มีการจับคู่ผลรวมในใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="8e7b4-104">One type of invoice matching validation is invoice totals matching.</span></span> <span data-ttu-id="8e7b4-105">เพื่อระบุว่าระบบควรดำเนินการจับคู่ผลรวมในใบแจ้งหนี้ หน้า **พารามิเตอร์บัญชีเจ้าหนี้** บนแท็บ **การตรวจสอบใบแจ้งหนี้** ให้ตั้งค่าตัวเลือก **จับคู่ผลรวมในใบแจ้งหนี้** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="8e7b4-105">To specify that the system should perform invoice totals matching, on the **Accounts payable parameters** page, on the **Invoice validation** tab, set the **Match invoice totals** option **Yes**.</span></span> 

<span data-ttu-id="8e7b4-106">คุณสามารถใช้การจับคู่ผลรวมในใบแจ้งหนี้เพื่อรับประกันว่ายอดรวมของใบแจ้งหนี้ไม่เบี่ยงเบนจากยอดเงินที่คาดไว้โดยมากกว่าผลต่างที่ยอมรับได้</span><span class="sxs-lookup"><span data-stu-id="8e7b4-106">You can use invoice totals matching to help guarantee that total invoice amounts don't deviate from expected amounts by more than an acceptable variance.</span></span> <span data-ttu-id="8e7b4-107">มีการเปรียบเทียบผลรวมหกรายการในหน้า **รายละเอียดการจับคู่ผลรวมในใบแจ้งหนี้**</span><span class="sxs-lookup"><span data-stu-id="8e7b4-107">Six totals are compared on the **Invoice totals matching details** page.</span></span> <span data-ttu-id="8e7b4-108">ถ้ารายการใดๆของผลรวมแตกต่างจากผลรวมใบสั่งซื้อที่สอดคล้องกันที่มีการคาดไว้ ความขัดแย้งในการจับคู่จะถูกแฟล็ก</span><span class="sxs-lookup"><span data-stu-id="8e7b4-108">If any one of the totals deviates from the expected corresponding purchase order total, a matching discrepancy is flagged.</span></span> 

<span data-ttu-id="8e7b4-109">เพื่อตรวจทานใบแจ้งหนี้ที่มีความขัดแย้งการจับคู่ผลรวม ในพื้นที่ทำงาน **รายการบัญชีใบแจ้งหนี้ของผู้จัดจำหน่าย** ให้คลิกไทล์ **ใบแจ้งหนี้ที่ค้างอยู่**</span><span class="sxs-lookup"><span data-stu-id="8e7b4-109">To review the invoice that has the totals matching discrepancies, in the **Vendor invoice entry** workspace, click the **Pending invoices** tile.</span></span> <span data-ttu-id="8e7b4-110">จากนั้น บนบานหน้าต่างการดำเนินการ บนแท็บ **ตรวจทาน** ให้คลิก **รายละเอียดการจับคู่**</span><span class="sxs-lookup"><span data-stu-id="8e7b4-110">Then, on the Action Pane, on the **Review** tab, click **Matching details**.</span></span> <span data-ttu-id="8e7b4-111">ถ้ามีการตรวจพบความขัดแย้งของการจับคู่ ไอคอนคำเตือนจะปรากฏขึ้นถัดจากยอดเงินใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="8e7b4-111">If matching discrepancies have been detected, warning icons appear next to the invoice amount.</span></span> <span data-ttu-id="8e7b4-112">คุณสามารถดูรายละเอียดเพิ่มเติมเกี่ยวกับผลรวม โดยการดูรายละเอียดการจับคู่ผลรวมในใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="8e7b4-112">You can view more detail about the totals by viewing the invoice totals matching details.</span></span> 

<span data-ttu-id="8e7b4-113">หลังจากที่คุณระบุความขัดแย้ง คุณอาจต้องติดต่อผู้จัดจำหน่ายถ้าคุณคิดว่าข้อมูลในใบแจ้งหนี้ไม่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="8e7b4-113">After you identify a discrepancy, you might have to contact the vendor if you think that the information on the invoice is incorrect.</span></span> <span data-ttu-id="8e7b4-114">จากนั้น คุณสามารถดำเนินงานหนึ่งรายการของการดำเนินการเหล่านี้ ขึ้นอยู่กับข้อตกลงที่คูณทำไว้กับผู้จัดจำหน่าย:</span><span class="sxs-lookup"><span data-stu-id="8e7b4-114">Depending on the resulting agreement with the vendor, you can then take one of these actions:</span></span>

-   <span data-ttu-id="8e7b4-115">ยอมรับความแตกต่างของราคาและลงรายการใบแจ้งหนี้ที่มีความขัดแย้งในการจับคู่</span><span class="sxs-lookup"><span data-stu-id="8e7b4-115">Accept the price difference, and post the invoice that has matching discrepancies.</span></span> <span data-ttu-id="8e7b4-116">ระบบของคุณอาจถูกตั้งค่าให้ต้องการการอนุมัติก่อน จึงจะสามารถลงรายการบัญชีถ้ามีความขัดแย้งของการจับคู่</span><span class="sxs-lookup"><span data-stu-id="8e7b4-116">Your system might be set up to require approval before it can post if there are matching discrepancies.</span></span> <span data-ttu-id="8e7b4-117">ในกรณีนี้ คุณต้องทำการอนุมัติความขัดแย้งในการจับคู่ และสามารถเลือกที่จะป้อนข้อคิดเห็นการอนุมัติ</span><span class="sxs-lookup"><span data-stu-id="8e7b4-117">In this case, you must approve the matching discrepancy and can optionally enter an approval comment.</span></span> <span data-ttu-id="8e7b4-118">จากนั้นคุณสามารถเลือกที่จะลงรายการบัญชีใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="8e7b4-118">You can then select to post the invoice.</span></span>
-   <span data-ttu-id="8e7b4-119">ปรับปรุงจำนวนใบแจ้งหนี้ให้เป็นจำนวนตามที่คาดไว้ และลงรายการใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="8e7b4-119">Revise the invoice amount to the expected amount, and post the invoice.</span></span>
-   <span data-ttu-id="8e7b4-120">ร้องขอเครดิตเต็มจำนวนและใบแจ้งหนี้ใหม่ที่แก้ไขแล้วจากผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="8e7b4-120">Request a full credit and a new, corrected invoice from the vendor.</span></span>

<span data-ttu-id="8e7b4-121">สำหรับข้อมูลเพิ่มเติม โปรดดู [ค้นคว้าหรือแก้ไขข้อยกเว้น](tasks/research-resolve-exceptions.md)</span><span class="sxs-lookup"><span data-stu-id="8e7b4-121">For more information, see [Research or resolve exceptions](tasks/research-resolve-exceptions.md).</span></span>



