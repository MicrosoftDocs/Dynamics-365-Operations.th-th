---
title: "ภาพรวมการกระทบยอดบัญชีธนาคารขั้นสูง"
description: "บทความนี้อธิบายขั้นตอนสำหรับกระบวนการกระทบยอดธนาคารขั้นสูง คุณลักษณะการกระทบยอดบัญชีธนาคารขั้นสูงช่วยคุณนำเข้าใบแจ้งยอดจากธนาคารที่สามารถกระทบยอดจากภายในธุรกรรมธนาคารโดยอัตโนมัติ"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 22104
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 6de9a0323a1351fe88ad9aa82305a78c85673efe
ms.contentlocale: th-th
ms.lasthandoff: 04/13/2018

---

# <a name="advanced-bank-reconciliation-overview"></a><span data-ttu-id="f21f2-104">ภาพรวมการกระทบยอดบัญชีธนาคารขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="f21f2-104">Advanced bank reconciliation overview</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="f21f2-105">บทความนี้อธิบายขั้นตอนสำหรับกระบวนการกระทบยอดธนาคารขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="f21f2-105">This article describes the flow for the advanced bank reconciliation process.</span></span> <span data-ttu-id="f21f2-106">คุณลักษณะการกระทบยอดบัญชีธนาคารขั้นสูงช่วยคุณนำเข้าใบแจ้งยอดจากธนาคารที่สามารถกระทบยอดจากภายในธุรกรรมธนาคารโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="f21f2-106">The advanced bank reconciliation feature lets you import bank statements that can be automatically reconciled from within bank transactions.</span></span>

<span data-ttu-id="f21f2-107">คุณลักษณะการกระทบยอดบัญชีธนาคารขั้นสูงช่วยให้คุณสามารถนำเข้าใบแจ้งยอดจากธนาคารได้</span><span class="sxs-lookup"><span data-stu-id="f21f2-107">The advanced bank reconciliation feature lets you import bank statements.</span></span> <span data-ttu-id="f21f2-108">จากนั้นใบแจ้งยอดจากธนาคารที่นำเข้าสามารถถูกกระทบยอดโดยอัตโนมัติจากภายในธุรกรรมธนาคาร</span><span class="sxs-lookup"><span data-stu-id="f21f2-108">The imported bank statement can then be automatically reconciled from within bank transactions.</span></span> <span data-ttu-id="f21f2-109">นี่เป็นขั้นตอนต่างๆในขั้นตอนการกระทบยอดบัญชีธนาคารขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="f21f2-109">Here are the steps in the advanced bank reconciliation flow.</span></span>

1.  <span data-ttu-id="f21f2-110">ตั้งค่าการนำเข้าใบแจ้งยอดจากธนาคาร</span><span class="sxs-lookup"><span data-stu-id="f21f2-110">Set up a bank statement import.</span></span>
    -   <span data-ttu-id="f21f2-111">นำเข้าใบแจ้งยอดจากธนาคารโดยใช้กรอบงานเอนทิตี้ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="f21f2-111">Import bank statements through the data entity framework.</span></span>
    -   <span data-ttu-id="f21f2-112">รูปแบบใบแจ้งยอดจากธนาคารโดยทั่วไปมีอยู่สามรูปแบบอยู่ใน: ISO20022 BAI2 และ MT940</span><span class="sxs-lookup"><span data-stu-id="f21f2-112">Three typical bank statement formats are built in: ISO20022, BAI2, and MT940.</span></span>
    -   <span data-ttu-id="f21f2-113">ฟังก์ชันสามารถถูกขยายให้เป็นรูปแบบใดก็ได้</span><span class="sxs-lookup"><span data-stu-id="f21f2-113">The functionality can be extended to any format.</span></span>

2.  <span data-ttu-id="f21f2-114">ตั้งค่าลำดับหมายเลขที่จะใช้สำหรับการกระทบยอดบัญชีธนาคารขั้นสูง และกำหนดกฎหารจับคู่การกระทบยอดบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="f21f2-114">Set up a number sequence to use for advanced bank reconciliation, and define the bank reconciliation matching rules.</span></span>
    -   <span data-ttu-id="f21f2-115">กฎการจับคู่การกระทบยอดคือ ชุดของเงื่อนไขที่ใช้ในการกรองรายการใบแจ้งยอดจากธนาคารและรายการธุรกรรมธนาคารของ Microsoft Dynamics 365 for Finance and Operations ในระหว่างกระบวนการกระทบยอด</span><span class="sxs-lookup"><span data-stu-id="f21f2-115">A reconciliation matching rule is a set of criteria that are used to filter bank statement lines and Microsoft Dynamics 365 for Finance and Operations bank transaction lines during the reconciliation process.</span></span> <span data-ttu-id="f21f2-116">ขึ้นอยู่กับแนวทางปฏิบัติทางธุรกิจของคุณ คุณสามารถตั้งค่ากฎการจับคู่มากกว่าหนึ่งกฎ เพื่อทำให้เป็นอัตโนมัติและเพิ่มประสิทธิภาพกระบวนการกระทบยอดของคุณ</span><span class="sxs-lookup"><span data-stu-id="f21f2-116">Depending on your business practice, you can set up more than one matching rule to automate and optimize your reconciliation process.</span></span>

3.  <span data-ttu-id="f21f2-117">กระทบยอดใบแจ้งยอดจากธนาคารกับธุรกรรมธนาคาร Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f21f2-117">Reconcile bank statements with Finance and Operations bank transactions.</span></span>
    -   <span data-ttu-id="f21f2-118">ดำเนินการจับคู่และการสร้างสมุดรายวันการกระทบยอดอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="f21f2-118">Perform automatic matching and creation of reconciliation journals.</span></span>
    -   <span data-ttu-id="f21f2-119">ดูใบแจ้งยอดจากธนาคารและธุรกรรมธนาคาร Finance and Operations โดยละเอียด</span><span class="sxs-lookup"><span data-stu-id="f21f2-119">View bank statements and Finance and Operations bank transactions side by side.</span></span>
    -   <span data-ttu-id="f21f2-120">ลงรายการบัญชีธุรกรรมธนาคารของ Finance and Operations โดยอัตโนมัติ ถ้าปรากฏบนใบแจ้งยอดจากธนาคาร แต่ไม่ปรากฏใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f21f2-120">Automatically post Finance and Operations bank transactions if they appear on a bank statement but don't appear in Finance and Operations.</span></span>
    -   <span data-ttu-id="f21f2-121">สร้างใบแจ้งยอดของการกระทบยอด</span><span class="sxs-lookup"><span data-stu-id="f21f2-121">Generate a reconciliation statement.</span></span>






