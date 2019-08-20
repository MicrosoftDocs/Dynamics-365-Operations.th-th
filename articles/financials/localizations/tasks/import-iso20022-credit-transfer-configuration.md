---
title: นำเข้าการตั้งค่าคอนฟิกการโอนย้ายเครดิต ISO20022
description: 'กระบวนงานนี้แสดงวิธีการนำเข้าการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์การชำระเงินของผู้จัดจำหน่าย '
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee7e69611d31d2577ebafdfc059b0936aef0520b
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 08/02/2019
ms.locfileid: "1848802"
---
# <a name="import-iso20022-credit-transfer-configuration"></a><span data-ttu-id="af57a-103">นำเข้าการตั้งค่าคอนฟิกการโอนย้ายเครดิต ISO20022</span><span class="sxs-lookup"><span data-stu-id="af57a-103">Import ISO20022 credit transfer configuration</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="af57a-104">กระบวนงานนี้แสดงวิธีการนำเข้าการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์การชำระเงินของผู้จัดจำหน่าย </span><span class="sxs-lookup"><span data-stu-id="af57a-104">This procedure shows how to import a vendor payment electronic reporting configuration.</span></span> <span data-ttu-id="af57a-105">รูปแบบการโอนย้ายเครดิต ISO 20022 ของเยอรมันถูกใช้เป็นตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="af57a-105">The German ISO 20022 credit transfer format is used as an example.</span></span> <span data-ttu-id="af57a-106">สามารถใช้กระบวนงานนี้สำหรับรูปแบบการรายงานทางอิเล็กทรอนิกส์อื่นๆ ที่พร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="af57a-106">This procedure can be used for other available electronic reporting format.</span></span> 

<span data-ttu-id="af57a-107">งานนี้ถูกสร้างขึ้นโดยใช้บริษัทข้อมูลสาธิต DEMF แต่คุณสามารถใช้บริษัทข้อมูลสาธิตใดก็ได้เพื่อทำให้งานนี้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="af57a-107">This task was created using the demo data company DEMF but you can use any demo data company to complete this task.</span></span>

<span data-ttu-id="af57a-108">นี่คืองานแรกจากงานห้ารายการ ที่จะอธิบายกระบวนการชำระเงินของผู้จัดจำหน่ายโดยใช้การตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="af57a-108">This is the first of five tasks, that together illustrate the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="af57a-109">กระบวนงานนี้ใช้สำหรับคุณลักษณะทั้ที่ถูกเพิ่มลงใน Dynamics 365 for Operations รุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="af57a-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="af57a-110">ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="af57a-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="af57a-111">ในรายการผู้ให้บริการการตั้งค่าคอนฟิกที่พร้อมใช้งาน เลือก Microsoft</span><span class="sxs-lookup"><span data-stu-id="af57a-111">In the list of available configuration providers, select Microsoft.</span></span>
3. <span data-ttu-id="af57a-112">คลิก กำหนดเป็นใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="af57a-112">Click Set active.</span></span>
4. <span data-ttu-id="af57a-113">คลิก ที่เก็บ</span><span class="sxs-lookup"><span data-stu-id="af57a-113">Click Repositories.</span></span>
5. <span data-ttu-id="af57a-114">คลิก เปิด</span><span class="sxs-lookup"><span data-stu-id="af57a-114">Click Open.</span></span>
6. <span data-ttu-id="af57a-115">คลิกแสดงตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="af57a-115">Click Show filters.</span></span>
7. <span data-ttu-id="af57a-116">ใช้ตัวกรองต่อไปนี้: ป้อนค่าตัวกรอง "การโอนย้ายเครดิต ISO20022 (DE)" ในฟิลด์ "ชื่อการตั้งค่าคอนฟิก" โดยใช้ตัวดำเนินการตัวกรอง "เริ่มต้นด้วย"</span><span class="sxs-lookup"><span data-stu-id="af57a-116">Apply the following filters: Enter a filter value of "ISO20022 Credit transfer (DE)" on the "Configuration name" field using the "begins with" filter operator</span></span>
    * <span data-ttu-id="af57a-117">อีกทางหนึ่งคือ คุณสามารถค้นหาการตั้งค่าคอนฟิกในรายการ เลือก และย้ายไปยังงานนำเข้า</span><span class="sxs-lookup"><span data-stu-id="af57a-117">Alternatively, you can find the configuration in the list, select it, and then move it to the Import task.</span></span>  
8. <span data-ttu-id="af57a-118">คลิก นำเข้า</span><span class="sxs-lookup"><span data-stu-id="af57a-118">Click Import.</span></span>
    * <span data-ttu-id="af57a-119">ถ้าปุ่มการนำเข้าไม่พร้อมใช้งาน หมายความว่าการตั้งค่าคอนฟิกนี้ถูกนำเข้าเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="af57a-119">If the Import button is not available, it means that the configuration has  already been imported.</span></span>  
9. <span data-ttu-id="af57a-120">คลิก ใช่</span><span class="sxs-lookup"><span data-stu-id="af57a-120">Click Yes.</span></span>

