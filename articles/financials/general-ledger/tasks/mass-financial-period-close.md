---
title: การปิดรอบระยะเวลาทางการเงินโดยรวม
description: หัวข้อนี้แสดงวิธีการระงับรอบระยะเวลา หรือปิดรอบระยะเวลาหรือนิติบุคคลที่มากกว่าหนึ่งรายการอย่างถาวรในแต่ละครั้ง
author: aprilolson
manager: AnnBe
ms.date: 08/16/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCalendar, LedgerPeriodModuleAccessControlUpdate, SysLookupPicklist, LedgerFiscalCalendarPeriodStatus
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 398a62e575010501291af3016553fc72fbc891de
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914641"
---
# <a name="mass-financial-period-close"></a><span data-ttu-id="95808-103">การปิดรอบระยะเวลาทางการเงินโดยรวม</span><span class="sxs-lookup"><span data-stu-id="95808-103">Mass financial period close</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="95808-104">หัวข้อนี้แสดงวิธีการระงับรอบระยะเวลา หรือปิดรอบระยะเวลาหรือนิติบุคคลที่มากกว่าหนึ่งรายการอย่างถาวรในแต่ละครั้ง</span><span class="sxs-lookup"><span data-stu-id="95808-104">This topic shows how to place a period on hold or permanently close a period or more than one legal entity at a time.</span></span> <span data-ttu-id="95808-105">นอกจากนี้ งานนี้จะแสดงวิธีการจำกัดกลุ่มผู้ใช้ที่ลงรายการบัญชีในโมดูลที่เฉพาะเจาะจง</span><span class="sxs-lookup"><span data-stu-id="95808-105">In addition, the task will show how to restrict user group posting to specific modules.</span></span>

1. <span data-ttu-id="95808-106">ในบานหน้าต่างนำทาง ไปที่ **โมดูล > บัญชีแยกประเภททั่วไป > การปิดรอบระยะเวลา > ปฏิทินบัญชีแยกประเภท**</span><span class="sxs-lookup"><span data-stu-id="95808-106">In the navigation pane, go to **Modules > General ledger > Period close > Ledger calendars**.</span></span> <span data-ttu-id="95808-107">โปรดทราบว่ารายการของนิติบุคคลที่แสดงจะขึ้นอยู่กับปฏิทินทางการเงินที่เลือกไว้ในหน้านั้นๆ </span><span class="sxs-lookup"><span data-stu-id="95808-107">Note that the list of legal entities displayed is dependent on the fiscal calendar selected on the page.</span></span> <span data-ttu-id="95808-108">เฉพาะนิติบุคคลที่ใช้ปฏิทินทางการเงินที่เลือกจะแสดงขึ้น</span><span class="sxs-lookup"><span data-stu-id="95808-108">Only legal entities using the selected fiscal calendar will display.</span></span>
2. <span data-ttu-id="95808-109">เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="95808-109">Select **Edit**.</span></span>
3. <span data-ttu-id="95808-110">เลือกรอบระยะเวลาที่คุณต้องการปรับเปลี่ยนสถานะ</span><span class="sxs-lookup"><span data-stu-id="95808-110">Select the period for which you want to modify the status.</span></span>
4. <span data-ttu-id="95808-111">เลือกนิติบุคคลที่คุณต้องการปรับปรุงสถานะ</span><span class="sxs-lookup"><span data-stu-id="95808-111">Select the legal entities for which you want to update the status.</span></span> <span data-ttu-id="95808-112">คุณสามารถเลือกนิติบุคคลทั้งหมดได้อย่างรวดเร็ว โดยการเลือกเครื่องหมายถูกทางด้านซ้ายบนของกริด</span><span class="sxs-lookup"><span data-stu-id="95808-112">You can quickly select all legal entities by selecting the check mark on the upper left side of the grid.</span></span>  
5. <span data-ttu-id="95808-113">เลือก **ปรับปรุงการเข้าถึงโมดูล** เพื่อกำหนดการเข้าถึงการลงรายการบัญชีไปยังโมดูลที่เลือก</span><span class="sxs-lookup"><span data-stu-id="95808-113">Select **Update module access** to define the posting access to a selected module.</span></span> <span data-ttu-id="95808-114">สามารถปรับปรุงสถานะโมดูลทีละรายการได้โดยการแก้ไขเรกคอร์ดในกริด </span><span class="sxs-lookup"><span data-stu-id="95808-114">The module status can also be updated one-by-one by editing the records in the grid.</span></span> <span data-ttu-id="95808-115">ปุ่มจะมีประโยชน์เมื่อคุณต้องการอัพเดตเรกคอร์ดของนิติบุคคลหลายรายการอย่างรวดเร็ว</span><span class="sxs-lookup"><span data-stu-id="95808-115">The button is useful when you want to quickly update multiple legal entity records.</span></span>  
6. <span data-ttu-id="95808-116">ในโมดูล **แอพลิเคชัน** ให้เลือกโมดูลที่คุณต้องการปรับปรุงสถานะ</span><span class="sxs-lookup"><span data-stu-id="95808-116">In the **Application** module, select the module that you want to update the status.</span></span> <span data-ttu-id="95808-117">คลิก **เลือก**</span><span class="sxs-lookup"><span data-stu-id="95808-117">Click **Select**.</span></span>
7. <span data-ttu-id="95808-118">ในระดับ **การเข้าถึง** เลือก **ทั้งหมด** **ไม่มี** หรือกลุ่มผู้ใช้เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="95808-118">In the **Access** level, select **All**, **None**, or a specific user group.</span></span> <span data-ttu-id="95808-119">คลิก **เลือก**</span><span class="sxs-lookup"><span data-stu-id="95808-119">Click **Select**.</span></span> <span data-ttu-id="95808-120">ทั้งหมดนี้บ่งชี้ว่า ผู้ใช้ทั้งหมดที่มีการแก้ไขในการเข้าถึงโมดูลสามารถลงรายการบัญชีถ้ารอบระยะเวลาเปิดอยู่ </span><span class="sxs-lookup"><span data-stu-id="95808-120">All indicates all users with edit access to the module can post if the period is open.</span></span> <span data-ttu-id="95808-121">ไม่มีสิ่งที่บ่งชี้ว่า ผู้ใช้ไม่สามารถลงรายการบัญชีไปที่โมดูลถ้ารอบระยะเวลาเปิดอยู่ </span><span class="sxs-lookup"><span data-stu-id="95808-121">None indicates that users cannot post to the module if the period is open.</span></span> <span data-ttu-id="95808-122">กลุ่มผู้ใช้เฉพาะบ่งชี้ว่า เฉพาะผู้ใช้ในกลุ่มเท่านั้นที่จะสามารถลงรายการบัญชีในโมดูลถ้ารอบระยะเวลาเปิดอยู่</span><span class="sxs-lookup"><span data-stu-id="95808-122">A specific user group indicates only users in the group are able to post to the module if the period is open.</span></span>  
8. <span data-ttu-id="95808-123">เลือก **ปรับปรุง**</span><span class="sxs-lookup"><span data-stu-id="95808-123">Select **Update**.</span></span>
9. <span data-ttu-id="95808-124">เลือกรอบระยะเวลาอื่นเพื่อปรับปรุงสถานะ</span><span class="sxs-lookup"><span data-stu-id="95808-124">Select another period to update the status.</span></span>
10. <span data-ttu-id="95808-125">เลือกนิติบุคคลที่คุณต้องการปรับปรุงสถานะรอบระยะเวลา</span><span class="sxs-lookup"><span data-stu-id="95808-125">Select the legal entites for which you want to update the period status.</span></span>
11. <span data-ttu-id="95808-126">เลือก **ปรับปรุงสถานะรอบระยะเวลา** และตั้งค่าสถานะเป็น **ระงับ** **เปิด** หรือ **ปิดอย่างถาวร**</span><span class="sxs-lookup"><span data-stu-id="95808-126">Select **Update period status** and set the status of **On hold**, **Open**, or **Permanently closed**.</span></span> <span data-ttu-id="95808-127">**เปิด** หมายถึงสามารถลงรายการบัญชีรอบระยะเวลาได้ ซึ่งทำให้ผู้ใช้มีสิทธิ์การเข้าถึง</span><span class="sxs-lookup"><span data-stu-id="95808-127">**Open** indicates the period can be posted to, provided the user has access.</span></span> <span data-ttu-id="95808-128">**ระงับ** หมายถึงไม่สามารถลงรายการบัญชีรอบระยะเวลาได้ แต่สามารถเปิดรอบระยะเวลาใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="95808-128">**On hold** means the period cannot be posted to, but the period can be reopened.</span></span> <span data-ttu-id="95808-129">**ปิดถาวร** หมายถึงปิดรอบระยะเวลาแล้ว และไม่สามารถเปิดได้อีก</span><span class="sxs-lookup"><span data-stu-id="95808-129">**Permanently closed** means the period is closed and can never be opened.</span></span> <span data-ttu-id="95808-130">ไม่สามารถลงรายการบัญชีการปรับปรุงได้ </span><span class="sxs-lookup"><span data-stu-id="95808-130">Adjustments cannot be posted.</span></span> <span data-ttu-id="95808-131">เราไม่แนะนำให้ตั้งค่ารอบระยะเวลาเป็น **ปิดถาวร** จนกว่าการปรับปรุงและการตรวจสอบทั้งหมดจะเสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="95808-131">We do not recommend setting a period to **Permanently closed** until all adjustments and audits are complete.</span></span>  
12. <span data-ttu-id="95808-132">เลือก **ปรับปรุง**</span><span class="sxs-lookup"><span data-stu-id="95808-132">Select **Update**.</span></span>

