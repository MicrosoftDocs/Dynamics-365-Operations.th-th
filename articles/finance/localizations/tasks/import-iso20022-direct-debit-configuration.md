---
title: นำเข้าการตั้งค่าคอนฟิกการหักบัญชีเงินฝากอัตโนมัติ ISO20022
description: 'กระบวนงานนี้อธิบายวิธีการนำเข้าการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์การชำระเงินของลูกค้า '
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
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 964f396625340d593a2fe3dd5be5a1b7da795e9a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5218769"
---
# <a name="import-iso20022-direct-debit-configuration"></a><span data-ttu-id="a96e2-103">นำเข้าการตั้งค่าคอนฟิกการหักบัญชีเงินฝากอัตโนมัติ ISO20022</span><span class="sxs-lookup"><span data-stu-id="a96e2-103">Import ISO20022 direct debit configuration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a96e2-104">กระบวนงานนี้อธิบายวิธีการนำเข้าการตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์การชำระเงินของลูกค้า </span><span class="sxs-lookup"><span data-stu-id="a96e2-104">This procedure demonstrates how to import a customer payment electronic reporting configuration.</span></span> <span data-ttu-id="a96e2-105">กระบวนงานนี้ใช้รูปแบบการหักบัญชีเงินฝากอัตโนมัติ ISO 20022 เป็นตัวอย่าง</span><span class="sxs-lookup"><span data-stu-id="a96e2-105">This procedure uses the ISO 20022 direct debit format as an example.</span></span> 



<span data-ttu-id="a96e2-106">กระบวนงานนี้ถูกสร้างขึ้นโดยใช้บริษัทข้อมูลสาธิต DEMF แต่คุณสามารถใช้บริษัทข้อมูลสาธิตใดก็ได้สำหรับวัตถุประสงค์นี้</span><span class="sxs-lookup"><span data-stu-id="a96e2-106">This procedure was created using the demo data company DEMF but you can use any demo data company for this purpose.</span></span>



<span data-ttu-id="a96e2-107">นี่คือกระบวนงานแรกจากกระบวนงานห้ารายการที่แสดงให้เห็นถึงขั้นตอนการชำระเงินโดยใช้การตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="a96e2-107">This is the first of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>

1. <span data-ttu-id="a96e2-108">ไปที่การจัดการองค์กร > พื้นที่ทำงาน > การรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="a96e2-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="a96e2-109">ในรายการผู้ให้บริการการตั้งค่าคอนฟิกที่พร้อมใช้งาน เลือก Microsoft</span><span class="sxs-lookup"><span data-stu-id="a96e2-109">In the list of available configuration providers, select Microsoft.</span></span>
3. <span data-ttu-id="a96e2-110">คลิก กำหนดเป็นใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="a96e2-110">Click Set active.</span></span>
4. <span data-ttu-id="a96e2-111">คลิก ที่เก็บ</span><span class="sxs-lookup"><span data-stu-id="a96e2-111">Click Repositories.</span></span>
5. <span data-ttu-id="a96e2-112">คลิก เปิด</span><span class="sxs-lookup"><span data-stu-id="a96e2-112">Click Open.</span></span>
6. <span data-ttu-id="a96e2-113">คลิกแสดงตัวกรอง</span><span class="sxs-lookup"><span data-stu-id="a96e2-113">Click Show filters.</span></span>
7. <span data-ttu-id="a96e2-114">ใช้ตัวกรองต่อไปนี้: ป้อนค่าตัวกรอง "การหักบัญชีเงินฝากอัตโนมัติ ISO20022 (DE)" ในฟิลด์ "ชื่อการตั้งค่าคอนฟิก" โดยใช้ตัวดำเนินการตัวกรอง "เริ่มต้นด้วย"</span><span class="sxs-lookup"><span data-stu-id="a96e2-114">Apply the following filters: Enter a filter value of "ISO20022 Direct debit (DE)" on the "Configuration name" field using the "begins with" filter operator</span></span>
    * <span data-ttu-id="a96e2-115">อีกทางหนึ่งคือ คุณสามารถหาการตั้งค่าคอนฟิกในรายการ เลือก และข้ามขั้นตอนนี้</span><span class="sxs-lookup"><span data-stu-id="a96e2-115">Optionally, you can find the configuration in the list, select it, and skip this step.</span></span>  
8. <span data-ttu-id="a96e2-116">คลิก นำเข้า</span><span class="sxs-lookup"><span data-stu-id="a96e2-116">Click Import.</span></span>
    * <span data-ttu-id="a96e2-117">ถ้าปุ่มการนำเข้าไม่พร้อมใช้งาน หมายความว่าการตั้งค่าคอนฟิกนี้ถูกนำเข้าเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="a96e2-117">If the Import button is not available, it means that the configuration has been imported already.</span></span>  
9. <span data-ttu-id="a96e2-118">คลิก ใช่</span><span class="sxs-lookup"><span data-stu-id="a96e2-118">Click Yes.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]