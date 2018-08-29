---
title: "ทำให้ตัวคั่นผังบัญชีไม่ซ้ำกัน"
description: "ใน Dynamics 365 for Finance and Operations คุณไม่สามารถมีตัวคั่นเดียวกันสำหรับผังบัญชีและค่ามิติได้ คุณต้องเปลี่ยนค่าตัวคั่นหลังจากการอัพเกรด"
author: ryansandness
manager: AnnBe
ms.date: 03/30/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: e197a1b44e038a97b8bf6db692dcc2eef2bc5f7b
ms.contentlocale: th-th
ms.lasthandoff: 08/09/2018

---

# <a name="make-the-chart-of-accounts-delimiter-unique"></a><span data-ttu-id="0cd02-104">ทำให้ตัวคั่นผังบัญชีไม่ซ้ำกัน</span><span class="sxs-lookup"><span data-stu-id="0cd02-104">Make the chart of accounts delimiter unique</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0cd02-105">ใน Microsoft Dynamics AX 2012 คุณสามารถใช้ตัวคั่นเดียวกันสำหรับผังบัญชีและค่ามิติได้</span><span class="sxs-lookup"><span data-stu-id="0cd02-105">In Microsoft Dynamics AX 2012, you could use the same delimiter for your chart of accounts and dimension values.</span></span> <span data-ttu-id="0cd02-106">ใน Dynamics 365 for Finance and Operations คุณไม่สามารถมีตัวคั่นเดียวกันสำหรับผังบัญชีและค่ามิติได้</span><span class="sxs-lookup"><span data-stu-id="0cd02-106">In Dynamics 365 for Finance and Operations, you cannot have the same delimiter for the chart of accounts and dimension values.</span></span> <span data-ttu-id="0cd02-107">ถ้าไม่มีตัวคั่นซ้ำ คุณสามารถเปลี่ยนได้หลังจากการอัพเกรด</span><span class="sxs-lookup"><span data-stu-id="0cd02-107">If there is a duplicate delimiter, you can change it after upgrade.</span></span> 

<span data-ttu-id="0cd02-108">คุณลักษณะนี้จะพร้อมใช้งานใน:</span><span class="sxs-lookup"><span data-stu-id="0cd02-108">This feature is available in:</span></span>
- <span data-ttu-id="0cd02-109">Dynamics 365 for Finance and Operations รุ่น 8.0</span><span class="sxs-lookup"><span data-stu-id="0cd02-109">Dynamics 365 for Finance and Operations version 8.0</span></span>
- <span data-ttu-id="0cd02-110">Dynamics 365 for Finance and Operations รุ่น 7.1 KB 4094701 ไม่สามารถป้อนมิติทางการเงินได้ เมื่อค่ามิติประกอบด้วยตัวคั่นผังบัญชี</span><span class="sxs-lookup"><span data-stu-id="0cd02-110">Dynamics 365 for Finance and Operations version 7.1, KB 4094701 Cannot enter the financial dimensions when the dimension values contain the chart of accounts delimiter</span></span>
- <span data-ttu-id="0cd02-111">Dynamics 365 for Finance and Operations รุ่น 7.2 KB 4092967 ไม่สามารถเลือกโครงการย่อยเป็นมิติได้ เมื่อรูปแบบของโครงการย่อยประกอบด้วยตัวคั่นมิติ</span><span class="sxs-lookup"><span data-stu-id="0cd02-111">Dynamics 365 for Finance and Operations version 7.2, KB 4092967 Cannot choose sub-project as dimension when sub-project format contains the dimension delimiter</span></span>

## <a name="update-delimiter"></a><span data-ttu-id="0cd02-112">อัพเดตตัวคั่น</span><span class="sxs-lookup"><span data-stu-id="0cd02-112">Update delimiter</span></span>
<span data-ttu-id="0cd02-113">ถ้ามีความขัดแย้งกับผังบัญชี สามารถเปลี่ยนตัวคั่นผังบัญชีตัวและรูปแบบรหัสโครงการ/โครงการย่อยได้</span><span class="sxs-lookup"><span data-stu-id="0cd02-113">If there is a conflict with the Chart of Accounts, the Chart of accounts delimiter and the project/subproject ID format can be changed.</span></span> <span data-ttu-id="0cd02-114">ไม่มีตัวคั่นมิติอื่นๆ ที่สามารถเปลี่ยนได้</span><span class="sxs-lookup"><span data-stu-id="0cd02-114">No other dimension delimiters can be changed.</span></span> 
- <span data-ttu-id="0cd02-115">คุณสามารถเปลี่ยนตัวคั่นผังบัญชีได้ หลังจากการอัพเกรดเป็น Finance and Operations ใน **พารามิเตอร์บัญชีแยกประเภททั่วไป** > **ผังบัญชีและมิติ** > **เปลี่ยนตัวคั่น**</span><span class="sxs-lookup"><span data-stu-id="0cd02-115">You can change the chart of accounts delimiter after upgrade to Finance and Operations in **General ledger parameters** > **Chart of accounts and dimensions** > **Change delimiter**.</span></span> 
- <span data-ttu-id="0cd02-116">ถ้ามีเฉพาะความขัดแย้งอยู่กับรูปแบบรหัสโครงการ/โครงการย่อย คุณสามารถเปลี่ยนค่านั้นได้ใน **พารามิเตอร์การจัดการและการบัญชีโครงการ** > **ทั่วไป** > **ปรับเปลี่ยนรูปแบบโครงการย่อย**</span><span class="sxs-lookup"><span data-stu-id="0cd02-116">If the only conflict is with the project/subproject ID format, you can change that value in **Project management and accounting parameters** > **General** > **Modify subproject format**.</span></span> 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a><span data-ttu-id="0cd02-117">วิธีการตรวจสอบว่า สภาพแวดล้อมของคุณต้องใช้ตัวคั่นที่มีการปรับปรุงหรือไม่</span><span class="sxs-lookup"><span data-stu-id="0cd02-117">How to determine if your environment requires updated delimiters</span></span> 
<span data-ttu-id="0cd02-118">ถ้าตัวคั่นในสภาพแวดล้อมที่มีการอัพเกรดของคุณขัดแย้งกัน คุณอาจพบความไม่มีเสถียรภาพ เมื่อป้อนค่าในตัวควบคุมรายการที่มีการแบ่งส่วนหรือตัวควบคุมรายการมิติ</span><span class="sxs-lookup"><span data-stu-id="0cd02-118">If delimiters in your upgraded environment are conflicting, you may experience instability when entering values in a segmented entry control or dimension entry control.</span></span> <span data-ttu-id="0cd02-119">ซึ่งหมายความว่า คุณจะต้องใช้การใช้การค้นหาหรือเมนูแบบลอยขึ้นเสมอ เมื่อป้อนชุดบัญชีและมิติ</span><span class="sxs-lookup"><span data-stu-id="0cd02-119">This means that you will need to always use lookups or a flyout menu when entering account and dimension combinations.</span></span>

