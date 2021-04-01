---
title: ภาพรวมการกระทบยอดบัญชีธนาคารขั้นสูง
description: บทความนี้อธิบายขั้นตอนสำหรับกระบวนการกระทบยอดธนาคารขั้นสูง คุณลักษณะการกระทบยอดบัญชีธนาคารขั้นสูงช่วยคุณนำเข้าใบแจ้งยอดจากธนาคารที่สามารถกระทบยอดจากภายในธุรกรรมธนาคารโดยอัตโนมัติ
author: panolte
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: roschlom
ms.custom: 22104
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1f85ece0b25237c194777b41566860c49d4b9d39
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5258219"
---
# <a name="advanced-bank-reconciliation-overview"></a><span data-ttu-id="e9578-104">ภาพรวมการกระทบยอดบัญชีธนาคารขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="e9578-104">Advanced bank reconciliation overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e9578-105">บทความนี้อธิบายขั้นตอนสำหรับกระบวนการกระทบยอดธนาคารขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="e9578-105">This article describes the flow for the advanced bank reconciliation process.</span></span> <span data-ttu-id="e9578-106">คุณลักษณะการกระทบยอดบัญชีธนาคารขั้นสูงช่วยคุณนำเข้าใบแจ้งยอดจากธนาคารที่สามารถกระทบยอดจากภายในธุรกรรมธนาคารโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="e9578-106">The advanced bank reconciliation feature lets you import bank statements that can be automatically reconciled from within bank transactions.</span></span>

<span data-ttu-id="e9578-107">คุณลักษณะการกระทบยอดบัญชีธนาคารขั้นสูงช่วยให้คุณสามารถนำเข้าใบแจ้งยอดจากธนาคารได้</span><span class="sxs-lookup"><span data-stu-id="e9578-107">The advanced bank reconciliation feature lets you import bank statements.</span></span> <span data-ttu-id="e9578-108">จากนั้นใบแจ้งยอดจากธนาคารที่นำเข้าสามารถถูกกระทบยอดโดยอัตโนมัติจากภายในธุรกรรมธนาคาร</span><span class="sxs-lookup"><span data-stu-id="e9578-108">The imported bank statement can then be automatically reconciled from within bank transactions.</span></span> <span data-ttu-id="e9578-109">นี่เป็นขั้นตอนต่างๆในขั้นตอนการกระทบยอดบัญชีธนาคารขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="e9578-109">Here are the steps in the advanced bank reconciliation flow.</span></span>

1.  <span data-ttu-id="e9578-110">ตั้งค่าการนำเข้าใบแจ้งยอดจากธนาคาร</span><span class="sxs-lookup"><span data-stu-id="e9578-110">Set up a bank statement import.</span></span>
    -   <span data-ttu-id="e9578-111">นำเข้าใบแจ้งยอดจากธนาคารโดยใช้กรอบงานเอนทิตี้ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="e9578-111">Import bank statements through the data entity framework.</span></span>
    -   <span data-ttu-id="e9578-112">รูปแบบใบแจ้งยอดจากธนาคารโดยทั่วไปมีอยู่สามรูปแบบอยู่ใน: ISO20022 BAI2 และ MT940</span><span class="sxs-lookup"><span data-stu-id="e9578-112">Three typical bank statement formats are built in: ISO20022, BAI2, and MT940.</span></span>
    -   <span data-ttu-id="e9578-113">ฟังก์ชันสามารถถูกขยายให้เป็นรูปแบบใดก็ได้</span><span class="sxs-lookup"><span data-stu-id="e9578-113">The functionality can be extended to any format.</span></span>

2.  <span data-ttu-id="e9578-114">ตั้งค่าลำดับหมายเลขที่จะใช้สำหรับการกระทบยอดบัญชีธนาคารขั้นสูง และกำหนดกฎหารจับคู่การกระทบยอดบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="e9578-114">Set up a number sequence to use for advanced bank reconciliation, and define the bank reconciliation matching rules.</span></span>
    -   <span data-ttu-id="e9578-115">กฎการจับคู่การกระทบยอดเป็นชุดของเกณฑ์ที่ถูกใช้เพื่อกรองรายการใบแจ้งยอดจากธนาคาร และธุรกรรมธนาคาร Microsoft Dynamics 365 Finance ในระหว่างกระบวนการกระทบยอด</span><span class="sxs-lookup"><span data-stu-id="e9578-115">A reconciliation matching rule is a set of criteria that are used to filter bank statement lines and Microsoft Dynamics 365 Finance bank transaction lines during the reconciliation process.</span></span> <span data-ttu-id="e9578-116">ขึ้นอยู่กับแนวทางปฏิบัติทางธุรกิจของคุณ คุณสามารถตั้งค่ากฎการจับคู่มากกว่าหนึ่งกฎ เพื่อทำให้เป็นอัตโนมัติและเพิ่มประสิทธิภาพกระบวนการกระทบยอดของคุณ</span><span class="sxs-lookup"><span data-stu-id="e9578-116">Depending on your business practice, you can set up more than one matching rule to automate and optimize your reconciliation process.</span></span>

3.  <span data-ttu-id="e9578-117">กระทบยอดใบแจ้งยอดจากธนาคารกับธุรกรรมธนาคาร Finance</span><span class="sxs-lookup"><span data-stu-id="e9578-117">Reconcile bank statements with Finance bank transactions.</span></span>
    -   <span data-ttu-id="e9578-118">ดำเนินการจับคู่และการสร้างสมุดรายวันการกระทบยอดอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="e9578-118">Perform automatic matching and creation of reconciliation journals.</span></span>
    -   <span data-ttu-id="e9578-119">ดูใบแจ้งยอดจากธนาคารและธุรกรรมธนาคาร Finance โดยละเอียด</span><span class="sxs-lookup"><span data-stu-id="e9578-119">View bank statements and Finance bank transactions side by side.</span></span>
    -   <span data-ttu-id="e9578-120">ลงรายการบัญชีธุรกรรมธนาคารของ Finance โดยอัตโนมัติ ถ้าปรากฏบนใบแจ้งยอดจากธนาคาร แต่ไม่ปรากฏในแอพ Finance</span><span class="sxs-lookup"><span data-stu-id="e9578-120">Automatically post Finance bank transactions if they appear on a bank statement but don't appear in the Finance app.</span></span>
    -   <span data-ttu-id="e9578-121">สร้างใบแจ้งยอดของการกระทบยอด</span><span class="sxs-lookup"><span data-stu-id="e9578-121">Generate a reconciliation statement.</span></span>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]