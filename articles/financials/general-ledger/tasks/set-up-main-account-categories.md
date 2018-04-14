--- 
title: "ตั้งค่าประเภทบัญชีหลัก"
description: "ประเภทบัญชีหลักจะใช้สำหรับรายงานเริ่มต้น ในการรายงานทางการเงิน และ ใน Power BI "
author: aprilolson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d67ca0f21388630ca7875b0cb647195a8344b80e
ms.contentlocale: th-th
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-main-account-categories"></a><span data-ttu-id="c5131-103">ตั้งค่าประเภทบัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="c5131-103">Set up main account categories</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c5131-104">ประเภทบัญชีหลักจะใช้สำหรับรายงานเริ่มต้น ในการรายงานทางการเงิน และ ใน Power BI </span><span class="sxs-lookup"><span data-stu-id="c5131-104">Main account categories are used for the default reports in financial reporting and in Power BI.</span></span> <span data-ttu-id="c5131-105">ประเภทบัญชีหลักที่ถูกสร้างขึ้น ตามค่าเริ่มต้นสามารถเปลี่ยนชื่อ แต่จะไม่ถูกไม่ลบ </span><span class="sxs-lookup"><span data-stu-id="c5131-105">Main account categories that are created by default can be renamed but not deleted.</span></span> <span data-ttu-id="c5131-106">ประเภทบัญชีหลักเพิ่มเติมสามารถสร้างขึ้นได้และใช้เพื่อการรายงานและการวิเคราะห์วัตถุประสงค์ </span><span class="sxs-lookup"><span data-stu-id="c5131-106">Additional account categories can be created and used for reporting and analysis purposes.</span></span> <span data-ttu-id="c5131-107">งานนี้ใช้บริษัทสาธิต USMF </span><span class="sxs-lookup"><span data-stu-id="c5131-107">This task uses the USMF demo company.</span></span>


## <a name="create-a-main-account-category"></a><span data-ttu-id="c5131-108">สร้างประเภทบัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="c5131-108">Create a main account category</span></span>
1. <span data-ttu-id="c5131-109">ไปที่ บัญชีแยกประเภททั่วไป > ผังบัญชี > บัญชี > ประเภทบัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="c5131-109">Go to General ledger > Chart of accounts > Accounts > Main account categories.</span></span>
2. <span data-ttu-id="c5131-110">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="c5131-110">Click New.</span></span>
3. <span data-ttu-id="c5131-111">ในฟิล์ประเภทบัญชีหลัก ให้ป้อนชื่อเฉพาะ</span><span class="sxs-lookup"><span data-stu-id="c5131-111">In the Main account category field, enter a unique name.</span></span>
4. <span data-ttu-id="c5131-112">ในฟิลด์คำอธิบาย ให้ป้อนคำอธิบายสำหรับประเภทบัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="c5131-112">In the Description field, enter a description for the main account category.</span></span>
5. <span data-ttu-id="c5131-113">ในชนิดบัญชีหลัก ให้เลือกชนิดบัญชีหลักที่จะเชื่อมโยงกับประเภท</span><span class="sxs-lookup"><span data-stu-id="c5131-113">In the Main account type field, select the main account type that will be linked to the category.</span></span>

## <a name="link-main-accounts-to-account-category"></a><span data-ttu-id="c5131-114">เชื่อมโยงบัญชีหลักกับประเภทบัญชี</span><span class="sxs-lookup"><span data-stu-id="c5131-114">Link main accounts to account category</span></span>
1. <span data-ttu-id="c5131-115">คลิก เชื่อมโยงบัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="c5131-115">Click Link main accounts.</span></span>
2. <span data-ttu-id="c5131-116">ในรายการนี้ เลือกบัญชีหลักที่จะกำหนดประเภทบัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="c5131-116">In the list, select the main accounts to assign to the main account category.</span></span>
    * <span data-ttu-id="c5131-117">การกำหนดบัญชีหลักให้กับประเภทบัญชีหลักจะรวมยอดดุลของบัญชีเมื่อใช้ประเภทสำหรับการวิเคราะห์และการรายงานทางการเงิน</span><span class="sxs-lookup"><span data-stu-id="c5131-117">Assigning main accounts to a main account category will aggregate the balances of the accounts when that category is used for financial reporting and analysis.</span></span>  
3. <span data-ttu-id="c5131-118">ให้เลือก หรือล้างตัวเลือกการเชื่อมโยงเพื่อเลือกบัญชีหลัก</span><span class="sxs-lookup"><span data-stu-id="c5131-118">Select or clear the Linked option to choose the main accounts.</span></span>
4. <span data-ttu-id="c5131-119">คลิก ตกลง ระบบจะนำเข้าข้อมูลการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="c5131-119">Click OK.</span></span>
5. <span data-ttu-id="c5131-120">คลิก ใช่</span><span class="sxs-lookup"><span data-stu-id="c5131-120">Click Yes.</span></span>


