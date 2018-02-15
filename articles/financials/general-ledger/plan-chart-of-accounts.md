---
title: "วางแผนชื่อผังบัญชีของคุณ"
description: "บทความนี้ให้ข้อมูลที่จะช่วยให้คุณวางแผนผังบัญชีสำหรับองค์กรของคุณ"
author: aprilolson
manager: AnnBe
ms.date: 01/04/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ad55dd57483de4351c8501c5e226180fc73606aa
ms.openlocfilehash: 3d2cdeaf2fdeb2f587f82c97249886fb8db49154
ms.contentlocale: th-th
ms.lasthandoff: 01/11/2018

---

# <a name="plan-your-chart-of-accounts"></a><span data-ttu-id="83b06-103">วางแผนชื่อผังบัญชีของคุณ</span><span class="sxs-lookup"><span data-stu-id="83b06-103">Plan your chart of accounts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="83b06-104">บทความนี้ให้ข้อมูลที่จะช่วยให้คุณวางแผนผังบัญชีสำหรับองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="83b06-104">This article provides information that will help you plan the chart of accounts for your organization.</span></span>

<span data-ttu-id="83b06-105">การติดตาม และรักษาข้อมูลทางการเงินในองค์กร คุณสามารถตั้งค่าผังบัญชี</span><span class="sxs-lookup"><span data-stu-id="83b06-105">To track and maintain financial information in an organization, you can set up a chart of accounts.</span></span> <span data-ttu-id="83b06-106">ผังบัญชีคือ ชุดของบัญชีที่กำหนดกรอบงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="83b06-106">A chart of accounts is a collection of accounts that define a financial framework.</span></span> <span data-ttu-id="83b06-107">การติดตามธุรกรรมในบัญชีเหล่านี้เพิ่มเติม คุณสามารถเพิ่มเซ็กเมนต์ ซึ่งเรียกว่ามิติทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="83b06-107">To further track the transactions in these accounts, you can add segments, which are known as financial dimensions.</span></span> <span data-ttu-id="83b06-108">ตัวอย่างเช่น บัญชีค่าใช้จ่ายอาจรวมถึงมิติทางการเงินที่มีชื่อแผนก ศูนย์ต้นทุน และวัตถุประสงค์ได้</span><span class="sxs-lookup"><span data-stu-id="83b06-108">For example, an expense account might include financial dimensions that are named Department, Cost center, and Purpose.</span></span> <span data-ttu-id="83b06-109">กฎผู้ใช้เป็นผู้กำหนด ที่ทราบว่าเป็นโครงสร้างทางบัญชีและกฎขั้นสูง กำหนดวิธีที่มิติทางการเงินถูกแนบกับบัญชีหลัก และมิติทางการเงินอื่น และวิธีป้อนธุรกรรม</span><span class="sxs-lookup"><span data-stu-id="83b06-109">User-defined rules, which are known as account structures and advanced rules, determine how financial dimensions are attached to the main accounts and other financial dimensions, and also how transactions are entered.</span></span> 

<span data-ttu-id="83b06-110">ผังบัญชีคือ โครงสร้างรายการของบัญชีแยกประเภททั่วไปของนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="83b06-110">The chart of accounts is a structured list of a legal entity’s general ledger accounts.</span></span> <span data-ttu-id="83b06-111">รายการถูกใช้เพื่อจัดทำรายงานทางการเงินสำหรับหน่วยจัดเก็บภาษีและเจ้าของ</span><span class="sxs-lookup"><span data-stu-id="83b06-111">The list is used to prepare financial reports for authorities and owners.</span></span> <span data-ttu-id="83b06-112">บัญชีจะถูกจัดกลุ่มเป็นชนิดของบัญชี และจากนั้นรวมเป็นประเภทที่ใหญ่กว่าต่อไป</span><span class="sxs-lookup"><span data-stu-id="83b06-112">The accounts are grouped into types of accounts and then further aggregated into larger categories.</span></span> <span data-ttu-id="83b06-113">ที่ระดับทั่วไปมากที่สุด บัญชีจะถูกจัดกลุ่มเป็นรายได้ และต้นทุน (บัญชีการดำเนินงาน) และสินทรัพย์ และหนี้สิน (บัญชียอดดุล)</span><span class="sxs-lookup"><span data-stu-id="83b06-113">At the most general level, the accounts are grouped as revenues and costs (operating accounts), and assets and liabilities (balance accounts).</span></span> 

<span data-ttu-id="83b06-114">ผังบัญชีสามารถใช้ร่วมกัน และใช้โดยนิติบุคคลใดๆ ในองค์กร </span><span class="sxs-lookup"><span data-stu-id="83b06-114">A chart of accounts can be shared and used by any legal entity in an organization.</span></span> <span data-ttu-id="83b06-115">กำหนดผังบัญชีที่ใช้โดยนิติบุคคลที่ถูกระบุบนหน้า **บัญชีแยกประเภท**</span><span class="sxs-lookup"><span data-stu-id="83b06-115">The chart of accounts that is used by a legal entity is defined on the **Ledger** page.</span></span> 

<span data-ttu-id="83b06-116">นี่คือบางส่วนของตัวแปรที่คุณต้องพิจารณาเมื่อคุณวางแผนโครงสร้างของผังบัญชีสำหรับองค์กรของคุณ:</span><span class="sxs-lookup"><span data-stu-id="83b06-116">Here are some of the factors that you must consider when you plan the structure of the chart of accounts for your organization:</span></span>

-   <span data-ttu-id="83b06-117">ความต้องการในการรายงานของประเทศ/ภูมิภาคที่บริษัทของคุณตั้งอยู่</span><span class="sxs-lookup"><span data-stu-id="83b06-117">The reporting requirements of the country/region where your organization is based</span></span>
-   <span data-ttu-id="83b06-118">ความต้องการรายงานของนิติบุคคลของคุณ</span><span class="sxs-lookup"><span data-stu-id="83b06-118">The reporting requirements of your legal entity</span></span>
-   <span data-ttu-id="83b06-119">ระดับข้อมูลจำเพาะที่จำเป็นสำหรับทั้งองค์กรภายนอกและสำหรับองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="83b06-119">The degree of specification that is required, both for both external organizations and for your organization</span></span>

<span data-ttu-id="83b06-120">สร้างผังบัญชีในหน้า **ผังบัญชี**</span><span class="sxs-lookup"><span data-stu-id="83b06-120">Create the chart of accounts on the **Chart of accounts** page.</span></span> <span data-ttu-id="83b06-121">สามารถสร้างบัญชีหลักจากหน้า **ผังบัญชี** หรือหน้า **บัญชีหลัก** ได้</span><span class="sxs-lookup"><span data-stu-id="83b06-121">Main accounts can be created from the **Chart of accounts** page or the **Main accounts** page.</span></span> <span data-ttu-id="83b06-122">บัญชีหลักของคุณไม่ควรใช้อักขระพิเศษใด ๆ ที่ใช้เป็นตัวกำหนดเขตผังบัญชี</span><span class="sxs-lookup"><span data-stu-id="83b06-122">Your main accounts shouldn't use any special characters that are used as chart of accounts delimiters.</span></span> <span data-ttu-id="83b06-123">หากคุณมีอักขระพิเศษที่เหมือนกับตัวกำหนดเขตผังบัญชี คุณอาจพบความไม่มีเสถียรภาพ หรือจำเป็นต้องใช้แถบลอยหรือค้นหาเสมอเมื่อป้อนบัญชีและชุดมิติ</span><span class="sxs-lookup"><span data-stu-id="83b06-123">If you do have a special character that is the same as your chart of accounts delimiter, you may experience instability, or the need to always use lookups or the flyout when entering account and dimension combinations.</span></span> <span data-ttu-id="83b06-124">สำหรับข้อมูลเพิ่มเติม โปรดดู [สร้างบัญชีหลัก](tasks/create-main-account.md)</span><span class="sxs-lookup"><span data-stu-id="83b06-124">For more information, see [Create a main account](tasks/create-main-account.md).</span></span>


<span data-ttu-id="83b06-125">เป็นความคิดที่ดีในการเชื่อมโยงบัญชีหลักกับประเภทบัญชีหลัก เพื่อให้คุณสามารถใช้ประโยชน์ของรายงานทางการเงินเริ่มต้นได้โดยไม่ต้องทำการปรับเปลี่ยนใด ๆ</span><span class="sxs-lookup"><span data-stu-id="83b06-125">It's a good idea to link the main accounts to main account categories, so that you can take advantage of the default financial reports without having to make any modifications.</span></span> <span data-ttu-id="83b06-126">ดังนั้น คุณสามารถออกแบบและรักษารายงานได้อย่างรวดเร็ว และง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="83b06-126">Therefore, you can more quickly and easily design and maintain reports.</span></span> 

<span data-ttu-id="83b06-127">ใช้หน้า **การตั้งค่าคอนฟิกโครงสร้างทางบัญชี** เพื่อสร้างโครงสร้างทางบัญชี</span><span class="sxs-lookup"><span data-stu-id="83b06-127">Use the **Configure account structures** page to create account structures.</span></span> <span data-ttu-id="83b06-128">โครงสร้างทางบัญชีกำหนดชุดที่ถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="83b06-128">Account structures define valid combinations.</span></span> <span data-ttu-id="83b06-129">การรวมกันกับบัญชีหลัก แบบฟอร์มผังบัญชี</span><span class="sxs-lookup"><span data-stu-id="83b06-129">The combinations, together with main accounts, form a chart of accounts.</span></span>  <span data-ttu-id="83b06-130">สำหรับข้อมูลเพิ่มเติม โปรดดู [สร้างโครงสร้างทางบัญชี](tasks/create-account-structures.md)</span><span class="sxs-lookup"><span data-stu-id="83b06-130">For more information, see [Create account structures](tasks/create-account-structures.md).</span></span>

<span data-ttu-id="83b06-131">**การแทนที่นิติบุคคล**</span><span class="sxs-lookup"><span data-stu-id="83b06-131">**Legal entity overrides**</span></span> 

<span data-ttu-id="83b06-132">ไม่ใช่บัญชีหลักทั้งหมดจะถูกต้องสำหรับทุกนิติบุคคล และบางมิติเท่านั้นอาจเกี่ยวข้องสำหรับรอบระยะเวลาเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="83b06-132">Not all main accounts are valid for all legal entities and some may only be relevant for a specific time period.</span></span> <span data-ttu-id="83b06-133">ในสถานการณ์ การแทนที่นิติบุคคลนี้สามารถนำมาใช้เพื่อระบุว่าบริษัทใดที่บัญชีหลักควรถูกหยุดชั่วคราว ใครคือเจ้าของ และรอบระยะเวลาที่มิติที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="83b06-133">In this scenario the Legal entity overrides section can be used to identify which companies the main account should be suspended for, who the owner is and the time period the dimension is active.</span></span> <span data-ttu-id="83b06-134">การแทนที่ในระดับที่ใช้ร่วมกันไม่สามารถจำกัดมากขึ้นกว่าการแทนที่ระดับนิติบุคคล</span><span class="sxs-lookup"><span data-stu-id="83b06-134">The overrides at the shared level cannot be more restrictive than the overrides at the legal entity level.</span></span>

<span data-ttu-id="83b06-135">สำหรับข้อมูลเพิ่มเติม โปรดดูหัวข้อต่อไปนี้: [มิติทางการเงิน](financial-dimensions.md)
[สร้างและกำหนดโครงสร้างกฎขั้นสูง](tasks/create-assign-advanced-rule-structures.md)</span><span class="sxs-lookup"><span data-stu-id="83b06-135">For more information, see the following topics: [Financial dimensions](financial-dimensions.md)
[Create and assign advanced rule structures](tasks/create-assign-advanced-rule-structures.md)</span></span>




