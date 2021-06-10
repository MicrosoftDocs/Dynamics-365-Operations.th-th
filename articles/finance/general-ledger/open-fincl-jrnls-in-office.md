---
title: เปิดเท็มเพลตสมุดรายวันทางการเงินใน Office
description: หัวข้อนี้อธิบายปัญหาที่อาจเกิดขึ้นเมื่อคุณสร้างสมุดรายวันทางการเงินที่กำหนดเองโดยใช้เท็มเพลต Microsoft Excel
author: kweekley
ms.date: 05/14/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0773f47551b2460ec310b92b67c634b433147749
ms.sourcegitcommit: 8c5b3e872825953853ad57fc67ba6e5ae92b9afe
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/24/2021
ms.locfileid: "6089468"
---
# <a name="open-financial-journal-templates-in-office"></a><span data-ttu-id="0cdee-103">เปิดเท็มเพลตสมุดรายวันทางการเงินใน Office</span><span class="sxs-lookup"><span data-stu-id="0cdee-103">Open financial journal templates in Office</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0cdee-104">หัวข้อนี้อธิบายปัญหาที่อาจเกิดขึ้นเมื่อคุณสร้างสมุดรายวันทางการเงินที่กำหนดเองโดยใช้เท็มเพลต Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="0cdee-104">This topic describes issues that might occur when you create custom financial journals by using a Microsoft Excel template.</span></span>

## <a name="symptom"></a><span data-ttu-id="0cdee-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="0cdee-105">Symptom</span></span>

<span data-ttu-id="0cdee-106">คุณสร้างเท็มเพลต Excel ที่กำหนดเองเป็นสมุดรายวันทางการเงิน แต่ไม่มีเท็มเพลตนั้นปรากฏในเมนู **เปิดรายการใน Excel**</span><span class="sxs-lookup"><span data-stu-id="0cdee-106">You created a custom Excel template for financial journals, but it doesn't appear on the **Open lines in Excel** menu.</span></span> <span data-ttu-id="0cdee-107">หรือเท็มเพลตนั้นปรากฏขึ้นบนเมนู แต่มีเท็มเพลตอื่นเปิดขึ้นเมื่อคุณเลือกเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="0cdee-107">Alternatively, it does appear on the menu, a different template is opened but when you select it.</span></span>

## <a name="resolution"></a><span data-ttu-id="0cdee-108">การแก้ปัญหา</span><span class="sxs-lookup"><span data-stu-id="0cdee-108">Resolution</span></span>

<span data-ttu-id="0cdee-109">ฟังก์ชันเปิดใน Excel เริ่มต้นจะใช้แหล่งข้อมูลราก (ตาราง) ของหน้าปัจจุบันเพื่อระบุว่าเท็มเพลต Office หรือเอนทิตี้ข้อมูลใดที่จะปรากฏเป็นตัวเลือกใน **เปิดใน Excel**</span><span class="sxs-lookup"><span data-stu-id="0cdee-109">The default Open in Excel functionality uses the root data source (table) of the current page to determine which Office templates or data entities appear as options on the **Open in Excel** menu.</span></span> <span data-ttu-id="0cdee-110">ลักษณะการทำงานนี้ไม่ใช่การใช้งานที่ดีสำหรับสมุดรายวันทางการเงิน เนื่องจากสมุดรายวันทางการเงินจะใช้ตารางเดียวกัน (LedgerJournalTable และ LedgerJournalTrans) เป็นแหล่งข้อมูลรากของสมุดรายวันชนิดอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="0cdee-110">This behavior isn't an ideal experience for financial journals, because financial journals use the same tables (LedgerJournalTable and LedgerJournalTrans) as the root data source of many other types of journals.</span></span>

<span data-ttu-id="0cdee-111">ฟังก์ชันเปิดรายการใน Excel ของสมุดรายงานทางการเงินมีวัตถุประสงค์เพื่อแสดงเท็มเพลตที่ออกแบบไว้ให้กับสมุดรายวันที่คุณใช้งานอยู่ในบริบทปัจจุบัน เช่น สมุดรายวันทั่วไปหรือสมุดรายวันการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="0cdee-111">For financial journals, the Open Lines in Excel functionality is intended to show templates that are designed for the journal that you're currently working in the context of, such as the general journal or a payment journal.</span></span> <span data-ttu-id="0cdee-112">ตัวอย่างเช่น เท็มเพลตที่มีวัตถุประสงค์เพื่อใช้กับสมุดรายวันการชำระเงินของผู้จัดจำหน่ายออกแบบมาเพื่อบังคับใช้บัญชีหลักของคุณเป็นบัญชีผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="0cdee-112">For example, a template that is intended to be used with a vendor payment journal will be designed to enforce your primary account as a vendor account.</span></span>

<span data-ttu-id="0cdee-113">ถ้าคุณต้องการเลื่อนระดับเท็มเพลตเพื่อให้เท็มเพลตสามารถใช้งานในเมนู **เปิดรายการใน Excel** และ **เปิดใน Excel** ประสบการณ์แบบง่ายๆ สำหรับนักพัฒนาคือการใช้งานอินเทอร์เฟส **LedgerIJournalExcelTemplate** และขยายคลาส **DocuTemplateRegistrationBase**</span><span class="sxs-lookup"><span data-stu-id="0cdee-113">If you want to promote a template so that it's available on the **Open lines in Excel** and **Open in Excel** menus, an easy developer experience is to implement the **LedgerIJournalExcelTemplate** interface and extend the **DocuTemplateRegistrationBase** class.</span></span> <span data-ttu-id="0cdee-114">หลายตัวอย่างของวิธีการนี้จะดําเนินการในระบบ</span><span class="sxs-lookup"><span data-stu-id="0cdee-114">Many examples of this approach are implemented in the system.</span></span> <span data-ttu-id="0cdee-115">ตัวอย่างหนึ่งที่สามารถใช้เพื่ออ้างอิงได้คืออินเทอร์เฟส **LedgerDailyJournalExcelTemplate** ที่สร้างขึ้นในสมุดรายวันทั่วไป (หรือสมุดรายวันประจำวัน)</span><span class="sxs-lookup"><span data-stu-id="0cdee-115">One example that can be used for reference is the **LedgerDailyJournalExcelTemplate** interface that was created for the general journal (or daily journal).</span></span>

<span data-ttu-id="0cdee-116">เมื่อมีการใช้งานอินเทอร์เฟส **LedgerIJournalExcelTemplate** กับเท็มเพลตของคุณ เมนู **เปิดรายการใน Excel** จะกรองเท็มเพลตตามชนิดสมุดรายวันของสมุดรายวันของคุณ และจะแสดงเฉพาะเท็มเพลตที่สามารถใช้งานได้กับสมุดรายวันเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="0cdee-116">When the **LedgerIJournalExcelTemplate** interface is implemented for your template, the **Open Lines in Excel** menu will filter templates by the journal type of your journal and will show only the templates that are available for that journal.</span></span> <span data-ttu-id="0cdee-117">อินเทอร์เฟสยังมีวิธีการตรวจสอบความถูกต้องที่ช่วยให้มั่นใจว่าไม่สามารถเปิดเท็มเพลตของสมุดรายวันได้หากเท็มเพลตไม่ตรงกับข้อกำหนดชนิดบัญชี</span><span class="sxs-lookup"><span data-stu-id="0cdee-117">The interface also provides a validation method that ensures that a template can't be opened for a journal if it doesn't meet the account type requirements.</span></span> <span data-ttu-id="0cdee-118">ตัวอย่างเช่น คุณสามารถระบุว่าชนิดบัญชีต้องเป็นชนิด **ผู้จัดจำหน่าย** หรือ **บัญชีแยกประเภท**</span><span class="sxs-lookup"><span data-stu-id="0cdee-118">For example, you can specify that the account type must be of the **Vendor** or **Ledger** type.</span></span>

<span data-ttu-id="0cdee-119">หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับฟังก์ชันนี้ โปรดดู [เพิ่มเท็มเพลตในเมนูเปิดรายการใน Excel](../../fin-ops-core/dev-itpro/user-interface/add-templates-open-lines-excel-menu.md)</span><span class="sxs-lookup"><span data-stu-id="0cdee-119">For more information about this functionality, see [Add templates to the Open lines in Excel menu](../../fin-ops-core/dev-itpro/user-interface/add-templates-open-lines-excel-menu.md).</span></span>
