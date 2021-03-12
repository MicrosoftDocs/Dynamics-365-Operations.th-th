---
title: สร้างกลุ่มการรวมบัญชีและบัญชีหลักในการรวมบัญชีเพิ่มเติม
description: 'ขั้นตอนนี้แสดงวิธีการสร้างกลุ่มบัญชีการรวมบัญชี และเพิ่มบัญชีให้กับกลุ่มนั้น '
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerConsolidateAccountGroup, MainAccountConsolidateAccount
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fbdfa340f25fdf90048a9a4696ccb20855435a7a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/15/2021
ms.locfileid: "4978650"
---
# <a name="create-consolidation-groups-and-additional-consolidation-accounts"></a><span data-ttu-id="861f0-103">สร้างกลุ่มการรวมบัญชีและบัญชีหลักในการรวมบัญชีเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="861f0-103">Create consolidation groups and additional consolidation accounts</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="861f0-104">ขั้นตอนนี้แสดงวิธีการสร้างกลุ่มบัญชีการรวมบัญชี และเพิ่มบัญชีให้กับกลุ่มนั้น </span><span class="sxs-lookup"><span data-stu-id="861f0-104">This procedure shows how to create a consolidation account group and then add accounts to the group.</span></span> <span data-ttu-id="861f0-105">ขั้นตอนนี้ใช้ข้อมูลบริษัทสาธิต USMF</span><span class="sxs-lookup"><span data-stu-id="861f0-105">This procedure uses the demo data company USMF.</span></span>


## <a name="create-a-consolidation-account-group"></a><span data-ttu-id="861f0-106">สร้างกลุ่มบัญชีการรวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="861f0-106">Create a consolidation account group</span></span>
1. <span data-ttu-id="861f0-107">ไปที่บัญชีแยกประเภททั่วไป > ผังบัญชี > บัญชี > กลุ่มบัญชีการรวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="861f0-107">Go to General ledger > Chart of accounts > Accounts > Consolidation account groups.</span></span>
2. <span data-ttu-id="861f0-108">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="861f0-108">Click New.</span></span>
3. <span data-ttu-id="861f0-109">ในฟิลด์กลุ่มบัญชีการรวมบัญชี ให้ป้อนรหัสเฉพาะตัวระบุสำหรับกลุ่มบัญชีการรวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="861f0-109">In the Consolidation account group field, enter a unique identifier for the consolidation account group.</span></span>
4. <span data-ttu-id="861f0-110">ในฟิลด์ชื่อ ให้พิมพ์ค่า </span><span class="sxs-lookup"><span data-stu-id="861f0-110">In the Name field, type a value.</span></span>

## <a name="add-accounts-to-consolidation-account-group"></a><span data-ttu-id="861f0-111">เพิ่มบัญชีลงในกลุ่มบัญชีหลักในการรวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="861f0-111">Add accounts to consolidation account group</span></span>
1. <span data-ttu-id="861f0-112">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="861f0-112">Close the page.</span></span>
2. <span data-ttu-id="861f0-113">ไปที่บัญชีแยกประเภททั่วไป > ผังบัญชี > บัญชี > บัญชีการรวมบัญชีเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="861f0-113">Go to General ledger > Chart of accounts > Accounts > Additional consolidation accounts.</span></span>
3. <span data-ttu-id="861f0-114">คลิก สร้าง</span><span class="sxs-lookup"><span data-stu-id="861f0-114">Click New.</span></span>
4. <span data-ttu-id="861f0-115">ในฟิลด์บัญชีหลัก ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="861f0-115">In the Main account field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="861f0-116">ในรายการ ให้คลิกบัญชีหลักที่คุณต้องการแม็ป </span><span class="sxs-lookup"><span data-stu-id="861f0-116">In the list, click the main account that you want to map.</span></span>
6. <span data-ttu-id="861f0-117">ในฟิลด์บัญชีหลักในการรวมบัญชี ให้คลิกปุ่มดรอปดาวน์เพื่อเปิดการค้นหา</span><span class="sxs-lookup"><span data-stu-id="861f0-117">In the Consolidation account group field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="861f0-118">ในรายการ ให้คลิกบัญชีหลักในการรวมบัญชี</span><span class="sxs-lookup"><span data-stu-id="861f0-118">In the list, click the consolidation account group.</span></span>
8. <span data-ttu-id="861f0-119">ในฟิลด์บัญชีหลักในการรวมบัญชี ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="861f0-119">In the Consolidation account field, type a value.</span></span>
9. <span data-ttu-id="861f0-120">ในฟิลด์ชื่อบัญชีหลักในการรวมบัญชี ให้พิมพ์ค่าใดค่าหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="861f0-120">In the Consolidation account name field, type a value.</span></span>

