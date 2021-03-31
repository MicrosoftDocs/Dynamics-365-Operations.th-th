---
title: กลุ่มบัญชีหลักในการรวมบัญชีและบัญชีหลักในการรวมบัญชีเพิ่มเติม
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับกลุ่มลูกค้าองค์กรการรวมและลูกค้าองค์กรการรวมเพิ่มเติม และอธิบายวิธีการใช้งานใน Microsoft Dynamics 365 Finance
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerConsolidateAccountGroup
audience: Application User
ms.reviewer: roschlom
ms.custom: 265544
ms.assetid: 71c31df7-b655-46a8-8844-4f92a8bd71b0
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 0f89ffda27ff29e03bb517dfb6e7bfebee716027
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210252"
---
# <a name="consolidation-account-groups-and-additional-consolidation-accounts"></a><span data-ttu-id="e8074-103">กลุ่มบัญชีหลักในการรวมบัญชีและบัญชีหลักในการรวมบัญชีเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="e8074-103">Consolidation account groups and additional consolidation accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e8074-104">หัวข้อนี้ให้ข้อมูลเกี่ยวกับกลุ่มลูกค้าองค์กรการรวมและลูกค้าองค์กรการรวมเพิ่มเติม และอธิบายวิธีการใช้งานใน Microsoft Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="e8074-104">This topic provides information about consolidation account groups and additional consolidation accounts, and explains how they are used in Microsoft Dynamics 365 Finance.</span></span>

<a name="consolidation-account-groups"></a><span data-ttu-id="e8074-105">กลุ่มบัญชีการรวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="e8074-105">Consolidation account groups</span></span>
----------------------------

<span data-ttu-id="e8074-106">กลุ่มบัญชีหลักในการรวมบัญชีช่วยให้คุณสามารถสร้างกลุ่มของบัญชีที่คุณต้องการใช้ในการรวมข้อมูล</span><span class="sxs-lookup"><span data-stu-id="e8074-106">Consolidation account groups let you create groups of the accounts that you want to use to consolidate data.</span></span> <span data-ttu-id="e8074-107">ส่วนใหญ่แล้ว กลุ่มบัญชีหลักในการรวมบัญชีแสดงถึงผังบัญชีตามข้อบังคับตามกฎหมาย หรือแม็ปบัญชีไปยังกลุ่มที่ถูกกำหนดโดยสำนักงานใหญ่ของบริษัท</span><span class="sxs-lookup"><span data-stu-id="e8074-107">Most often, a consolidation account group represents a government-mandated chart of accounts or maps accounts to a group that is defined by the company's headquarters.</span></span> <span data-ttu-id="e8074-108">คุณสามารถค้นหากลุ่มบัญชีหลักในการรวมบัญชีได้ในพื้นที่ **การตั้งค่า** ของโมดูล **การรวมบัญชี** ได้</span><span class="sxs-lookup"><span data-stu-id="e8074-108">You can find consolidation account groups in the **Setup** area of the **Consolidations** module.</span></span> <span data-ttu-id="e8074-109">เมื่อคุณเพิ่มกลุ่มใหม่ คุณจะต้องป้อนตัวระบุเฉพาะสำหรับกลุ่มบัญชีและชื่อ</span><span class="sxs-lookup"><span data-stu-id="e8074-109">When you add a new group, you enter a unique identifier for the account group and a name.</span></span>

## <a name="additional-consolidation-accounts"></a><span data-ttu-id="e8074-110">บัญชีการรวมบัญชีเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="e8074-110">Additional consolidation accounts</span></span>
<span data-ttu-id="e8074-111">บัญชีหลักในการรวมบัญชีเพิ่มเติมช่วยให้คุณสามารถกำหนดบัญชีจากผังบัญชีที่มีอยู่ไปยังกลุ่มบัญชีหลักในการรวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="e8074-111">Additional consolidation accounts let you assign an account from an existing chart of accounts to a consolidation account group.</span></span> <span data-ttu-id="e8074-112">จากนั้นคุณสามารถระบุค่าบัญชีหลักในการรวมบัญชีและชื่อ</span><span class="sxs-lookup"><span data-stu-id="e8074-112">You can then specify a consolidation account value and name.</span></span> 

<span data-ttu-id="e8074-113">คุณสามารถค้นหาบัญชีหลักในการรวมบัญชีเพิ่มเติมได้ในพื้นที่ **การตั้งค่า** ของโมดูล **การรวมบัญชี** ได้</span><span class="sxs-lookup"><span data-stu-id="e8074-113">You can find additional consolidation accounts in the **Setup** area of the **Consolidations** module.</span></span> <span data-ttu-id="e8074-114">เมื่อคุณสร้างบัญชีหลักในการรวมบัญชีใหม่ คุณต้องระบุข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="e8074-114">When you create a new consolidation account, you must specify the following information:</span></span>

-   <span data-ttu-id="e8074-115">**บัญชีหลัก** – ฟิลด์นี้เป็นการค้นหาที่แสดงบัญชีหลักทั้งหมดที่ยึดตามผังบัญชีที่คุณเลือกบนหน้านั้น</span><span class="sxs-lookup"><span data-stu-id="e8074-115">**Main account** – This field is a lookup that shows all the main accounts that are based on the chart of accounts that you selected on the page.</span></span> <span data-ttu-id="e8074-116">เมื่อคุณเลือกบัญชีผู้ใช้ ชื่อจะถูกป้อนโดยอัตโนมัติในฟิลด์ **ชื่อบัญชีหลัก**</span><span class="sxs-lookup"><span data-stu-id="e8074-116">When you select an account, the name is automatically entered in the **Main account name** field.</span></span>
-   <span data-ttu-id="e8074-117">**กลุ่มบัญชีหลักในการรวมบัญชี** – ใช้ฟิลด์นี้เพื่อระบุกลุ่มที่จะกำหนดบัญชี</span><span class="sxs-lookup"><span data-stu-id="e8074-117">**Consolidation account group** – Use this field to specify the group to assign the account to.</span></span> <span data-ttu-id="e8074-118">ถ้าคุณรวมสองวิธีที่แตกต่างกัน คุณต้องเพิ่มบัญชีเดียวกันไปยังกลุ่มบัญชีหลักในการรวมบัญชีทั้งสี่</span><span class="sxs-lookup"><span data-stu-id="e8074-118">If you consolidate in two different ways, you must add the same account to all four consolidation account groups.</span></span>
-   <span data-ttu-id="e8074-119">**บัญชีหลักในการรวมบัญชี** – ป้อนค่าของบัญชีหลักในการรวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="e8074-119">**Consolidation account** – Enter the value of the consolidation account.</span></span> <span data-ttu-id="e8074-120">ค่านี้ไม่จำเป็นต้องเป็นบัญชีจากผังบัญชี</span><span class="sxs-lookup"><span data-stu-id="e8074-120">This value doesn't have to be an account from a chart of accounts.</span></span> <span data-ttu-id="e8074-121">อาจเป็นค่าใดๆ ก็ได้ที่คุณต้องการ</span><span class="sxs-lookup"><span data-stu-id="e8074-121">It can be any value that you require.</span></span>
-   <span data-ttu-id="e8074-122">**ชื่อบัญชีหลักในการรวมบัญชี** – ป้อนชื่อบัญชีตามที่คุณต้องการให้ปรากฏในแบบสอบถามและรายงาน</span><span class="sxs-lookup"><span data-stu-id="e8074-122">**Consolidation account name** – Enter the name of account as you want it to appear on inquiries and reports.</span></span>
-   <span data-ttu-id="e8074-123">**ระดับ SAT** – ฟิลด์นี้ถูกใช้ในการรายงานใบแจ้งยอดบัญชีไปยังหน่วยงานภาษีของเม็กซิโก</span><span class="sxs-lookup"><span data-stu-id="e8074-123">**SAT level** – This field is used to report account statements to the Mexican tax authorities.</span></span> 

<span data-ttu-id="e8074-124">เมื่อคุณสร้างกลุ่มบัญชีหลักในการรวมบัญชีและบัญชีหลักในการรวมบัญชีเพิ่มเติมของคุณเสร็จสิ้น คุณสามารถเลือกกลุ่มในกระบวนการรวมบัญชีทางออนไลน์</span><span class="sxs-lookup"><span data-stu-id="e8074-124">When you've finished creating your consolidation account groups and additional consolidation accounts, you can select the group in the Consolidate online process.</span></span>


<span data-ttu-id="e8074-125">สำหรับข้อมูลเพิ่มเติม โปรดดู [สร้างกลุ่มการรวมบัญชีและบัญชีหลักในการรวมบัญชีเพิ่มเติม](../general-ledger/tasks/create-consolidation-groups.md)</span><span class="sxs-lookup"><span data-stu-id="e8074-125">For more information, see [Create consolidation groups and additional consolidation accounts](../general-ledger/tasks/create-consolidation-groups.md).</span></span> 





[!INCLUDE[footer-include](../../includes/footer-banner.md)]