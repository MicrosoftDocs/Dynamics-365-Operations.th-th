---
title: ลงรายการบัญชีรายงานค่าใช้จ่าย
description: หัวข้อนี้อธิบายวิธีการลงรายการบัญชีรายงานค่าใช้จ่ายในบัญชีแยกประเภททั่วไป
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d008ef8dd55550431fbb9e329cd7d9428a08831
ms.sourcegitcommit: ef08bf1258aefb525d56bf85ef19311be26ab94c
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 07/30/2019
ms.locfileid: "1794967"
---
# <a name="post-an-expense-report"></a><span data-ttu-id="2db9c-103">ลงรายการบัญชีรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="2db9c-103">Post an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2db9c-104">หลังจากที่อนุมัติและโอนย้ายรายงานค่าใช้จ่ายไปยังสมุดรายวันทั่วไปแล้ว จะสามารถลงรายการบัญชีรายงานนั้นในบัญชีแยกประเภททั่วไปได้</span><span class="sxs-lookup"><span data-stu-id="2db9c-104">After an expense report has been approved and transferred to the general journal, it can be posted to the general ledger.</span></span> <span data-ttu-id="2db9c-105">เมื่อคุณลงรายการบัญชีรายงาน จะมีการระบุค่าใช้จ่ายที่มีสิทธิ์สำหรับการขอคืนภาษีมูลค่าเพิ่ม (VAT)</span><span class="sxs-lookup"><span data-stu-id="2db9c-105">When you post an expense report, expenses that are eligible for recovery of value-added tax (VAT) are identified.</span></span> <span data-ttu-id="2db9c-106">มีการกำหนดงานของการตรวจสอบและการเรียกคืนการชำระ VAT ให้กับพนักงานที่รับผิดชอบการตรวจสอบรายงานค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="2db9c-106">The task of verifying and recovering VAT payments is assigned to the employee who is responsible for verifying the expense report.</span></span>

<span data-ttu-id="2db9c-107">ถ้ามีการเรียกเก็บค่าใช้จ่ายในรายงานค่าใช้จ่ายไปยังบริษัทอื่น นอกเหนือจากบริษัทที่จ้างพนักงาน คุณต้องตรวจสอบบริษัทที่จะได้รับชำระค่าใช้จ่ายดังกล่าวและบริษัทที่มีการค้างชำระค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="2db9c-107">If expenses on an expense report are charged to a company other than the company that employs the employee, you must verify the company that those expenses are owed to and the company that the expenses are owed from.</span></span> <span data-ttu-id="2db9c-108">ตัวอย่างเช่น พนักงานที่ส่งรายงานค่าใช้จ่ายทำงานสำหรับบริษัท DAT แต่คิดค่าใช้จ่ายไปยังบริษัท DIR</span><span class="sxs-lookup"><span data-stu-id="2db9c-108">For example, the employee who submitted an expense report works for the DAT company but charged an expense to the DIR company.</span></span> <span data-ttu-id="2db9c-109">ในกรณีนี้ DAT เป็นบริษัทที่จะได้รับชำระค่าใช้จ่าย และ DIR เป็นบริษัทที่มีการค้างชำระค่าใช้จ่าย</span><span class="sxs-lookup"><span data-stu-id="2db9c-109">In this case, DAT is the company that the expense is owed to, and DIR is the company that the expense is owed from.</span></span> <span data-ttu-id="2db9c-110">หลังจากที่คุณตรวจสอบรายการสมุดรายวันเหล่านี้ คุณสามารถลงรายการบัญชีรายการค่าใช้จ่ายในบัญชีแยกประเภททั่วไปได้</span><span class="sxs-lookup"><span data-stu-id="2db9c-110">After you verify these journal lines, you can post the expense lines to the general ledger.</span></span>

<span data-ttu-id="2db9c-111">ในการลงรายการบัญชีรายงานค่าใช้จ่าย บนหน้า **รายงานค่าใช้จ่ายที่อนุมัติ** เลือกรายงานค่าใช้จ่าย และจากนั้น บนบานหน้าต่างการดำเนินการ เลือก **ลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="2db9c-111">To post an expense report, on the **Approved expense reports** page, select the expense report, and then, on the Action Pane, select **Post**.</span></span>

<span data-ttu-id="2db9c-112">คุณยังสามารถลงรายการรายงานค่าใช้จ่ายทั้งหมดได้ในรายการในเวลาเดียวกันอีกด้วย</span><span class="sxs-lookup"><span data-stu-id="2db9c-112">You can also post all the expense reports in the list at the same time.</span></span> <span data-ttu-id="2db9c-113">เลือกรายงานค่าใช้จ่ายทั้งหมด และจากนั้น เลือก **ลงรายการบัญชี**</span><span class="sxs-lookup"><span data-stu-id="2db9c-113">Select all the expense reports, and then select **Post**.</span></span>
