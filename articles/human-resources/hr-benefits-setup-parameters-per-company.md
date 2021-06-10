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
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d2c564f0dfd1cbe44566269c97218450fedf2173
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/18/2021
ms.locfileid: "6057633"
---
# <a name="configure-benefits-management-parameters-per-company"></a><span data-ttu-id="e90cf-103">ตั้งค่าคอนฟิกพารามิเตอร์การจัดการสวัสดิการสำหรับแต่ละบริษัท</span><span class="sxs-lookup"><span data-stu-id="e90cf-103">Configure Benefits management parameters per company</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="e90cf-104">สำหรับแต่ละองค์กรที่มีสวัสดิการ คุณต้องตั้งค่าคอนฟิกการตั้งค่าสำหรับอีเมลการยืนยันสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="e90cf-104">For each organization that offers benefits, you must configure settings for benefits confirmation emails.</span></span>

## <a name="configure-confirmation-email-settings"></a><span data-ttu-id="e90cf-105">ตั้งค่าคอนฟิกการตั้งค่าอีเมลการยืนยัน</span><span class="sxs-lookup"><span data-stu-id="e90cf-105">Configure confirmation email settings</span></span>

1. <span data-ttu-id="e90cf-106">ในพื้นที่ทำงาน **การจัดการสิทธิประโยชน์** ภายใต้ **การตั้งค่า** ให้เลือก **พารามิเตอร์ทรัพยากรบุคคล**</span><span class="sxs-lookup"><span data-stu-id="e90cf-106">In the **Benefits management** workspace, under **Setup**, select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="e90cf-107">ในแท็บ **การจัดการสวัสดิการ** ระบุค่าในฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="e90cf-107">In the **Benefits management** tab, specify values for the following fields:</span></span> 

   | <span data-ttu-id="e90cf-108">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="e90cf-108">Field</span></span> | <span data-ttu-id="e90cf-109">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="e90cf-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="e90cf-110">**ส่งอีเมลการยืนยัน**</span><span class="sxs-lookup"><span data-stu-id="e90cf-110">**Send confirmation email**</span></span> | <span data-ttu-id="e90cf-111">เมื่อมีการเปิดใช้งานคุณลักษณะนี้ จะมีการส่งอีเมลการยืนยันให้กับพนักงาน เมื่อพวกเขาตรวจดูจากประสบการณ์ในการลงทะเบียนสวัสดิการในการบริการตนเองของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="e90cf-111">When this feature is on, a confirmation email will be sent to employees when they check out from the benefits enrollment experience in Employee self-service.</span></span> |
   | <span data-ttu-id="e90cf-112">**เท็มเพลตอีเมลการยืนยัน**</span><span class="sxs-lookup"><span data-stu-id="e90cf-112">**Confirmation email template**</span></span> | <span data-ttu-id="e90cf-113">เลือกเท็มเพลตอีเมลขององค์กรที่จะใช้ เมื่อส่งการยืนยันการลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="e90cf-113">Select the organization email template to use when sending the enrollment confirmation.</span></span> <span data-ttu-id="e90cf-114">ถ้าคุณไม่เลือกเท็มเพลต จะมีการส่งอีเมลทั่วไปต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="e90cf-114">If you don't select a template, the following generic email will be sent:</span></span><br><br><span data-ttu-id="e90cf-115">%EmployeeFirstName%</span><span class="sxs-lookup"><span data-stu-id="e90cf-115">%EmployeeFirstName%,</span></span><br><br><span data-ttu-id="e90cf-116">ขอแสดงความยินดี</span><span class="sxs-lookup"><span data-stu-id="e90cf-116">Congratulations!</span></span> <span data-ttu-id="e90cf-117">คุณได้ทำการลงทะเบียนสวัสดิการเสร็จเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="e90cf-117">You’ve successfully completed benefits enrollment.</span></span><br><br><span data-ttu-id="e90cf-118">ขอบคุณ</span><span class="sxs-lookup"><span data-stu-id="e90cf-118">Thank you,</span></span><br><span data-ttu-id="e90cf-119"><Company/Org name> สวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="e90cf-119"><Company/Org name> Benefits.</span></span> |
   | <span data-ttu-id="e90cf-120">**ที่อยู่อีเมลผู้ส่งเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="e90cf-120">**Default email sender address**</span></span> | <span data-ttu-id="e90cf-121">ที่อยู่อีเมลที่จะใช้เมื่อส่งอีเมลยืนยัน</span><span class="sxs-lookup"><span data-stu-id="e90cf-121">The email address to use when sending the confirmation email.</span></span> |

3. <span data-ttu-id="e90cf-122">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="e90cf-122">Select **Save**.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]