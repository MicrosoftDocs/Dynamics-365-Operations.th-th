---
title: ตั้งค่าประเภทบัญชีหลัก
description: หัวข้อนี้อธิบายวิธีการตั้งค่าประเภทบัญชีหลักใน Dynamics 365 Finance
author: aprilolson
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MainAccountCategory, MainAccountCategoryLink
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 957fdc184410dc85f54cd3163799a9003f0727bb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222234"
---
# <a name="set-up-main-account-categories"></a><span data-ttu-id="64c75-103">ตั้งค่าประเภทบัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="64c75-103">Set up main account categories</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="64c75-104">หัวข้อนี้อธิบายวิธีการตั้งค่าประเภทบัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="64c75-104">This topic explains how to set up main account categories.</span></span> <span data-ttu-id="64c75-105">ประเภทลูกค้าองค์กรหลักถูกใช้สำหรับรายงานเริ่มต้นในการรายงานทางการเงินและใน Power BI</span><span class="sxs-lookup"><span data-stu-id="64c75-105">Main account categories are used for the default reports in financial reporting and in Power BI.</span></span> <span data-ttu-id="64c75-106">ประเภทบัญชีหลักที่ถูกสร้างขึ้น ตามค่าเริ่มต้นสามารถเปลี่ยนชื่อ แต่จะไม่ถูกไม่ลบ </span><span class="sxs-lookup"><span data-stu-id="64c75-106">Main account categories that are created by default can be renamed but not deleted.</span></span> <span data-ttu-id="64c75-107">ประเภทบัญชีหลักเพิ่มเติมสามารถสร้างขึ้นได้และใช้เพื่อการรายงานและการวิเคราะห์วัตถุประสงค์ </span><span class="sxs-lookup"><span data-stu-id="64c75-107">Additional account categories can be created and used for reporting and analysis purposes.</span></span> <span data-ttu-id="64c75-108">หัวข้อนี้ใช้บริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="64c75-108">This topic uses the USMF demo company.</span></span>

## <a name="create-a-main-account-category"></a><span data-ttu-id="64c75-109">สร้างประเภทบัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="64c75-109">Create a main account category</span></span>
1. <span data-ttu-id="64c75-110">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > บัญชีแยกประเภททั่วไป > ผังบัญชี > บัญชี > ประเภทบัญชีหลัก**</span><span class="sxs-lookup"><span data-stu-id="64c75-110">In the navigation pane, go to **Modules > General Ledger > Chart of accounts > Accounts > Main account categories**.</span></span>
2. <span data-ttu-id="64c75-111">เลือก **ใหม่**</span><span class="sxs-lookup"><span data-stu-id="64c75-111">Select **New**.</span></span>
3. <span data-ttu-id="64c75-112">ในฟิลด์ **ประเภทบัญชีหลัก** ป้อนชื่อเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="64c75-112">In the **Main account category** field, enter a unique name.</span></span>
4. <span data-ttu-id="64c75-113">ใน **ฟิลด์คำอธิบาย** ให้ป้อนคำอธิบายสำหรับประเภทบัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="64c75-113">In the **Description field**, enter a description for the main account category.</span></span>
5. <span data-ttu-id="64c75-114">ใน **ชนิดบัญชีหลัก** ให้เลือกชนิดบัญชีหลักที่จะเชื่อมโยงกับประเภท</span><span class="sxs-lookup"><span data-stu-id="64c75-114">In the **Main account type** field, select the main account type that will be linked to the category.</span></span>

## <a name="link-main-accounts-to-account-category"></a><span data-ttu-id="64c75-115">เชื่อมโยงบัญชีหลักกับประเภทบัญชี</span><span class="sxs-lookup"><span data-stu-id="64c75-115">Link main accounts to account category</span></span>
1. <span data-ttu-id="64c75-116">คลิก **เชื่อมโยงบัญชีหลัก**</span><span class="sxs-lookup"><span data-stu-id="64c75-116">Click **Link main accounts**.</span></span>
2. <span data-ttu-id="64c75-117">ในรายการ ให้เลือกบัญชีหลักที่จะกำหนดให้กับประเภทบัญชีหลักโดยการเลือกกล่องกาเครื่องหมายในคอลัมน์ **ที่เชื่อมโยง**</span><span class="sxs-lookup"><span data-stu-id="64c75-117">In the list, select the main accounts to assign to the main account category by checking the boxes in the **Linked** column.</span></span> <span data-ttu-id="64c75-118">การกำหนดบัญชีหลักให้กับประเภทบัญชีหลักจะรวมยอดดุลของบัญชีเมื่อใช้ประเภทสำหรับการวิเคราะห์และการรายงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="64c75-118">Assigning main accounts to a main account category will aggregate the balances of the accounts when that category is used for financial reporting and analysis.</span></span>  
3. <span data-ttu-id="64c75-119">เลือกหรือล้างตัวเลือก **ที่เชื่อมโยง** ให้เลือกบัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="64c75-119">Select or clear the **Linked** option to choose the main accounts.</span></span>
4. <span data-ttu-id="64c75-120">เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="64c75-120">Select **OK**.</span></span>
5. <span data-ttu-id="64c75-121">เลือก **ใช่**</span><span class="sxs-lookup"><span data-stu-id="64c75-121">Select **Yes**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]