---
title: ตั้งค่าคอนฟิกพารามิเตอร์การจัดการสวัสดิการสำหรับแต่ละบริษัท
description: ตั้งค่าคอนฟิกพารามิเตอร์สำหรับการจัดการสวัสดิการสำหรับแต่ละบริษัทใน Microsoft Dynamics 365 Human Resources
author: andreabichsel
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 87d4f1e7580b333fd17d3b779aafa47c5baed424
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805669"
---
# <a name="configure-benefits-management-parameters-per-company"></a><span data-ttu-id="d05c0-103">ตั้งค่าคอนฟิกพารามิเตอร์การจัดการสวัสดิการสำหรับแต่ละบริษัท</span><span class="sxs-lookup"><span data-stu-id="d05c0-103">Configure Benefits management parameters per company</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="d05c0-104">สำหรับแต่ละองค์กรที่มีสวัสดิการ คุณต้องตั้งค่าคอนฟิกการตั้งค่าสำหรับอีเมลการยืนยันสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="d05c0-104">For each organization that offers benefits, you must configure settings for benefits confirmation emails.</span></span>

## <a name="configure-confirmation-email-settings"></a><span data-ttu-id="d05c0-105">ตั้งค่าคอนฟิกการตั้งค่าอีเมลการยืนยัน</span><span class="sxs-lookup"><span data-stu-id="d05c0-105">Configure confirmation email settings</span></span>

1. <span data-ttu-id="d05c0-106">ในพื้นที่ทำงาน **การจัดการสิทธิประโยชน์** ภายใต้ **การตั้งค่า** ให้เลือก **พารามิเตอร์ทรัพยากรบุคคล**</span><span class="sxs-lookup"><span data-stu-id="d05c0-106">In the **Benefits management** workspace, under **Setup**, select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="d05c0-107">ในแท็บ **การจัดการสวัสดิการ** ระบุค่าในฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d05c0-107">In the **Benefits management** tab, specify values for the following fields:</span></span> 

   | <span data-ttu-id="d05c0-108">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="d05c0-108">Field</span></span> | <span data-ttu-id="d05c0-109">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="d05c0-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="d05c0-110">**ส่งอีเมลการยืนยัน**</span><span class="sxs-lookup"><span data-stu-id="d05c0-110">**Send confirmation email**</span></span> | <span data-ttu-id="d05c0-111">เมื่อมีการเปิดใช้งานคุณลักษณะนี้ จะมีการส่งอีเมลการยืนยันให้กับพนักงาน เมื่อพวกเขาตรวจดูจากประสบการณ์ในการลงทะเบียนสวัสดิการในการบริการตนเองของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="d05c0-111">When this feature is on, a confirmation email will be sent to employees when they check out from the benefits enrollment experience in Employee self-service.</span></span> |
   | <span data-ttu-id="d05c0-112">**เท็มเพลตอีเมลการยืนยัน**</span><span class="sxs-lookup"><span data-stu-id="d05c0-112">**Confirmation email template**</span></span> | <span data-ttu-id="d05c0-113">เลือกเท็มเพลตอีเมลขององค์กรที่จะใช้ เมื่อส่งการยืนยันการลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="d05c0-113">Select the organization email template to use when sending the enrollment confirmation.</span></span> <span data-ttu-id="d05c0-114">ถ้าคุณไม่เลือกเท็มเพลต จะมีการส่งอีเมลทั่วไปต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d05c0-114">If you don't select a template, the following generic email will be sent:</span></span><br><br><span data-ttu-id="d05c0-115">%EmployeeFirstName%</span><span class="sxs-lookup"><span data-stu-id="d05c0-115">%EmployeeFirstName%,</span></span><br><br><span data-ttu-id="d05c0-116">ขอแสดงความยินดี</span><span class="sxs-lookup"><span data-stu-id="d05c0-116">Congratulations!</span></span> <span data-ttu-id="d05c0-117">คุณได้ทำการลงทะเบียนสวัสดิการเสร็จเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="d05c0-117">You’ve successfully completed benefits enrollment.</span></span><br><br><span data-ttu-id="d05c0-118">ขอบคุณ</span><span class="sxs-lookup"><span data-stu-id="d05c0-118">Thank you,</span></span><br><span data-ttu-id="d05c0-119"><Company/Org name> สวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="d05c0-119"><Company/Org name> Benefits.</span></span> |
   | <span data-ttu-id="d05c0-120">**ที่อยู่อีเมลผู้ส่งเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="d05c0-120">**Default email sender address**</span></span> | <span data-ttu-id="d05c0-121">ที่อยู่อีเมลที่จะใช้เมื่อส่งอีเมลยืนยัน</span><span class="sxs-lookup"><span data-stu-id="d05c0-121">The email address to use when sending the confirmation email.</span></span> |

3. <span data-ttu-id="d05c0-122">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="d05c0-122">Select **Save**.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]