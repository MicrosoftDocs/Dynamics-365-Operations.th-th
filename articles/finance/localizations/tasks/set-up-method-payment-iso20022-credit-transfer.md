---
title: การตั้งค่าวิธีการชำระเงินสำหรับการโอนย้ายเครดิต ISO20022
description: 'กระบวนงานนี้แสดงวิธีการตั้งค่าวิธีการชำระเงินของผู้จัดจำหน่ายการโอนย้ายเครดิต ISO20022 หรือชนิดการชำระเงินอื่นๆ โดยใช้การรายงานทางอิเล็กทรอนิกส์ในการสร้างไฟล์ '
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 643be31db625d0db12f1df18b9e797013da98ece
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832483"
---
# <a name="set-up-method-of-payment-for-iso20022-credit-transfer"></a><span data-ttu-id="073c6-103">การตั้งค่าวิธีการชำระเงินสำหรับการโอนย้ายเครดิต ISO20022</span><span class="sxs-lookup"><span data-stu-id="073c6-103">Set up method of payment for ISO20022 credit transfer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="073c6-104">กระบวนงานนี้แสดงวิธีการตั้งค่าวิธีการชำระเงินของผู้จัดจำหน่ายการโอนย้ายเครดิต ISO20022 หรือชนิดการชำระเงินอื่นๆ โดยใช้การรายงานทางอิเล็กทรอนิกส์ในการสร้างไฟล์ </span><span class="sxs-lookup"><span data-stu-id="073c6-104">This procedure shows how to set up the vendor method of payment for ISO20022 credit transfer or any other payment type using electronic reporting to generate a file.</span></span> 

<span data-ttu-id="073c6-105">ก่อนที่คุณจะทำงานนี้ให้เสร็จสมบูรณ์ คุณจะต้องส่งออกการตั้งค่าคอนฟิกรูปแบบและตั้งค่าบัญชีการชำระเงินก่อน</span><span class="sxs-lookup"><span data-stu-id="073c6-105">Before you complete this task, you must export format configurations and set up payment accounts.</span></span>

<span data-ttu-id="073c6-106">การทำงานนี้ถูกสร้างขึ้นโดยใช้บริษัทข้อมูลสาธิต DEMF</span><span class="sxs-lookup"><span data-stu-id="073c6-106">This task was created using the DEMF demo data company.</span></span>

<span data-ttu-id="073c6-107">นี่คือกระบวนงานที่สามจากกระบวนงานห้ารายการที่อธิบายกระบวนการชำระเงินของผู้จัดจำหน่ายโดยใช้การตั้งค่าคอนฟิกการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="073c6-107">This is the third procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="073c6-108">กระบวนงานนี้ใช้สำหรับคุณลักษณะทั้ที่ถูกเพิ่มลงใน Dynamics 365 for Operations รุ่น 1611</span><span class="sxs-lookup"><span data-stu-id="073c6-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="073c6-109">ไปที่บัญชีเจ้าหนี้ > การตั้งค่าการชำระเงิน > วิธีการชำระเงิน</span><span class="sxs-lookup"><span data-stu-id="073c6-109">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
2. <span data-ttu-id="073c6-110">ใช้ตัวกรองข้อมูลด่วนเพื่อค้นหาเรกคอร์ด </span><span class="sxs-lookup"><span data-stu-id="073c6-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="073c6-111">เช่น กรองข้อมูลขั้นตอนการชำระเงินในฟิลด์ ด้วยค่า 'SEPA CT'</span><span class="sxs-lookup"><span data-stu-id="073c6-111">For example, filter on the Method of payment field with a value of 'SEPA CT'.</span></span>
3. <span data-ttu-id="073c6-112">คลิกแก้ไข</span><span class="sxs-lookup"><span data-stu-id="073c6-112">Click Edit.</span></span>
4. <span data-ttu-id="073c6-113">ในฟิลด์รอบระยะเวลา เลือก 'ทั้งหมด'</span><span class="sxs-lookup"><span data-stu-id="073c6-113">In the Period field, select 'Total'.</span></span>
5. <span data-ttu-id="073c6-114">ในฟิลด์ชนิดการชำระเงิน เลือก 'การชำระเงินทางอิเล็กทรอนิกส์'</span><span class="sxs-lookup"><span data-stu-id="073c6-114">In the Payment type field, select 'Electronic payment'.</span></span>
6. <span data-ttu-id="073c6-115">ขยายส่วนรูปแบบของไฟล์</span><span class="sxs-lookup"><span data-stu-id="073c6-115">Expand the File formats section.</span></span>
7. <span data-ttu-id="073c6-116">เลือก ใช่ ในฟิลด์รายงานอิเล็กทรอนิกส์ทั่วไป</span><span class="sxs-lookup"><span data-stu-id="073c6-116">Select Yes in the Generic electronic reporting field.</span></span>
8. <span data-ttu-id="073c6-117">ในฟิลด์การตั้งค่าคอนฟิกรูปแบบการส่งออก ให้ป้อนหรือเลือกค่า</span><span class="sxs-lookup"><span data-stu-id="073c6-117">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="073c6-118">ในรายการ เลือกค่าการโอนย้ายเครดิต ISO20022 (DE)</span><span class="sxs-lookup"><span data-stu-id="073c6-118">In the list, select the value ISO20022 Credit transfer (DE).</span></span> <span data-ttu-id="073c6-119">ถ้ารายการว่างเปล่า จะไม่มีการนำเข้าหรือใช้งานการตั้งค่าคอนฟิกรูปแบบการส่งออกของการชำระเงินของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="073c6-119">If the list is empty, the vendor payment export format configuration is not imported and active.</span></span>  
9. <span data-ttu-id="073c6-120">ในประเภทบัญชี เลือก 'ธนาคาร'</span><span class="sxs-lookup"><span data-stu-id="073c6-120">In the Account type field, select 'Bank'.</span></span>
10. <span data-ttu-id="073c6-121">ในฟิลด์บัญชีการชำระเงิน ให้ระบุค่า 'DEMF OPER'</span><span class="sxs-lookup"><span data-stu-id="073c6-121">In the Payment account field, specify the values 'DEMF OPER'.</span></span>
11. <span data-ttu-id="073c6-122">คลิก บันทึก</span><span class="sxs-lookup"><span data-stu-id="073c6-122">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]