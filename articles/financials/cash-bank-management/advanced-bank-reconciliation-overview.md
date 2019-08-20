---
title: ภาพรวมการกระทบยอดบัญชีธนาคารขั้นสูง
description: บทความนี้อธิบายขั้นตอนสำหรับกระบวนการกระทบยอดธนาคารขั้นสูง คุณลักษณะการกระทบยอดบัญชีธนาคารขั้นสูงช่วยคุณนำเข้าใบแจ้งยอดจากธนาคารที่สามารถกระทบยอดจากภายในธุรกรรมธนาคารโดยอัตโนมัติ
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 22104
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5c76b38e957c1c76a80c76782f45405573b7f191
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842628"
---
# <a name="advanced-bank-reconciliation-overview"></a><span data-ttu-id="68a08-104">ภาพรวมการกระทบยอดบัญชีธนาคารขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="68a08-104">Advanced bank reconciliation overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="68a08-105">บทความนี้อธิบายขั้นตอนสำหรับกระบวนการกระทบยอดธนาคารขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="68a08-105">This article describes the flow for the advanced bank reconciliation process.</span></span> <span data-ttu-id="68a08-106">คุณลักษณะการกระทบยอดบัญชีธนาคารขั้นสูงช่วยคุณนำเข้าใบแจ้งยอดจากธนาคารที่สามารถกระทบยอดจากภายในธุรกรรมธนาคารโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="68a08-106">The advanced bank reconciliation feature lets you import bank statements that can be automatically reconciled from within bank transactions.</span></span>

<span data-ttu-id="68a08-107">คุณลักษณะการกระทบยอดบัญชีธนาคารขั้นสูงช่วยให้คุณสามารถนำเข้าใบแจ้งยอดจากธนาคารได้</span><span class="sxs-lookup"><span data-stu-id="68a08-107">The advanced bank reconciliation feature lets you import bank statements.</span></span> <span data-ttu-id="68a08-108">จากนั้นใบแจ้งยอดจากธนาคารที่นำเข้าสามารถถูกกระทบยอดโดยอัตโนมัติจากภายในธุรกรรมธนาคาร</span><span class="sxs-lookup"><span data-stu-id="68a08-108">The imported bank statement can then be automatically reconciled from within bank transactions.</span></span> <span data-ttu-id="68a08-109">นี่เป็นขั้นตอนต่างๆในขั้นตอนการกระทบยอดบัญชีธนาคารขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="68a08-109">Here are the steps in the advanced bank reconciliation flow.</span></span>

1.  <span data-ttu-id="68a08-110">ตั้งค่าการนำเข้าใบแจ้งยอดจากธนาคาร</span><span class="sxs-lookup"><span data-stu-id="68a08-110">Set up a bank statement import.</span></span>
    -   <span data-ttu-id="68a08-111">นำเข้าใบแจ้งยอดจากธนาคารโดยใช้กรอบงานเอนทิตี้ข้อมูล</span><span class="sxs-lookup"><span data-stu-id="68a08-111">Import bank statements through the data entity framework.</span></span>
    -   <span data-ttu-id="68a08-112">รูปแบบใบแจ้งยอดจากธนาคารโดยทั่วไปมีอยู่สามรูปแบบอยู่ใน: ISO20022 BAI2 และ MT940</span><span class="sxs-lookup"><span data-stu-id="68a08-112">Three typical bank statement formats are built in: ISO20022, BAI2, and MT940.</span></span>
    -   <span data-ttu-id="68a08-113">ฟังก์ชันสามารถถูกขยายให้เป็นรูปแบบใดก็ได้</span><span class="sxs-lookup"><span data-stu-id="68a08-113">The functionality can be extended to any format.</span></span>

2.  <span data-ttu-id="68a08-114">ตั้งค่าลำดับหมายเลขที่จะใช้สำหรับการกระทบยอดบัญชีธนาคารขั้นสูง และกำหนดกฎหารจับคู่การกระทบยอดบัญชีธนาคาร</span><span class="sxs-lookup"><span data-stu-id="68a08-114">Set up a number sequence to use for advanced bank reconciliation, and define the bank reconciliation matching rules.</span></span>
    -   <span data-ttu-id="68a08-115">กฎการจับคู่การกระทบยอดเป็นชุดของเกณฑ์ที่ถูกใช้เพื่อกรองรายการใบแจ้งยอดจากธนาคาร และธุรกรรมธนาคาร Microsoft Dynamics 365 for Finance and Operations ในระหว่างกระบวนการกระทบยอด</span><span class="sxs-lookup"><span data-stu-id="68a08-115">A reconciliation matching rule is a set of criteria that are used to filter bank statement lines and Microsoft Dynamics 365 for Finance and Operations bank transaction lines during the reconciliation process.</span></span> <span data-ttu-id="68a08-116">ขึ้นอยู่กับแนวทางปฏิบัติทางธุรกิจของคุณ คุณสามารถตั้งค่ากฎการจับคู่มากกว่าหนึ่งกฎ เพื่อทำให้เป็นอัตโนมัติและเพิ่มประสิทธิภาพกระบวนการกระทบยอดของคุณ</span><span class="sxs-lookup"><span data-stu-id="68a08-116">Depending on your business practice, you can set up more than one matching rule to automate and optimize your reconciliation process.</span></span>

3.  <span data-ttu-id="68a08-117">กระทบยอดใบแจ้งยอดจากธนาคารกับธุรกรรมธนาคาร Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="68a08-117">Reconcile bank statements with Finance and Operations bank transactions.</span></span>
    -   <span data-ttu-id="68a08-118">ดำเนินการจับคู่และการสร้างสมุดรายวันการกระทบยอดอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="68a08-118">Perform automatic matching and creation of reconciliation journals.</span></span>
    -   <span data-ttu-id="68a08-119">ดูใบแจ้งยอดจากธนาคารและธุรกรรมธนาคาร Finance and Operations โดยละเอียด</span><span class="sxs-lookup"><span data-stu-id="68a08-119">View bank statements and Finance and Operations bank transactions side by side.</span></span>
    -   <span data-ttu-id="68a08-120">ลงรายการบัญชีธุรกรรมธนาคารของ Finance and Operations โดยอัตโนมัติ ถ้าปรากฏบนใบแจ้งยอดจากธนาคาร แต่ไม่ปรากฏใน Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="68a08-120">Automatically post Finance and Operations bank transactions if they appear on a bank statement but don't appear in Finance and Operations.</span></span>
    -   <span data-ttu-id="68a08-121">สร้างใบแจ้งยอดของการกระทบยอด</span><span class="sxs-lookup"><span data-stu-id="68a08-121">Generate a reconciliation statement.</span></span>





