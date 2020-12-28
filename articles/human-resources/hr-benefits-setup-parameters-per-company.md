---
title: ตั้งค่าคอนฟิกพารามิเตอร์การจัดการสวัสดิการสำหรับแต่ละบริษัท
description: ตั้งค่าคอนฟิกพารามิเตอร์สำหรับการจัดการสวัสดิการสำหรับแต่ละบริษัทใน Microsoft Dynamics 365 Human Resources
author: andreabichsel
manager: tfehr
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
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
ms.openlocfilehash: 2943d0095e4c9421725b90e579b7cbb841038ab7
ms.sourcegitcommit: fd097f6f76f0d8428038fa3655b3188bf093b517
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/08/2020
ms.locfileid: "4692756"
---
# <a name="configure-benefits-management-parameters-per-company"></a><span data-ttu-id="79e8e-103">ตั้งค่าคอนฟิกพารามิเตอร์การจัดการสวัสดิการสำหรับแต่ละบริษัท</span><span class="sxs-lookup"><span data-stu-id="79e8e-103">Configure Benefits management parameters per company</span></span>

<span data-ttu-id="79e8e-104">สำหรับแต่ละองค์กรที่มีสวัสดิการ คุณต้องตั้งค่าคอนฟิกการตั้งค่าสำหรับอีเมลการยืนยันสวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="79e8e-104">For each organization that offers benefits, you must configure settings for benefits confirmation emails.</span></span>

## <a name="configure-confirmation-email-settings"></a><span data-ttu-id="79e8e-105">ตั้งค่าคอนฟิกการตั้งค่าอีเมลการยืนยัน</span><span class="sxs-lookup"><span data-stu-id="79e8e-105">Configure confirmation email settings</span></span>

1. <span data-ttu-id="79e8e-106">ในพื้นที่ทำงาน **การจัดการสิทธิประโยชน์** ภายใต้ **การตั้งค่า** ให้เลือก **พารามิเตอร์ทรัพยากรบุคคล**</span><span class="sxs-lookup"><span data-stu-id="79e8e-106">In the **Benefits management** workspace, under **Setup**, select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="79e8e-107">ในแท็บ **การจัดการสวัสดิการ** ระบุค่าในฟิลด์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="79e8e-107">In the **Benefits management** tab, specify values for the following fields:</span></span> 

   | <span data-ttu-id="79e8e-108">ฟิลด์</span><span class="sxs-lookup"><span data-stu-id="79e8e-108">Field</span></span> | <span data-ttu-id="79e8e-109">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="79e8e-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="79e8e-110">**ส่งอีเมลการยืนยัน**</span><span class="sxs-lookup"><span data-stu-id="79e8e-110">**Send confirmation email**</span></span> | <span data-ttu-id="79e8e-111">เมื่อมีการเปิดใช้งานคุณลักษณะนี้ จะมีการส่งอีเมลการยืนยันให้กับพนักงาน เมื่อพวกเขาตรวจดูจากประสบการณ์ในการลงทะเบียนสวัสดิการในการบริการตนเองของพนักงาน</span><span class="sxs-lookup"><span data-stu-id="79e8e-111">When this feature is on, a confirmation email will be sent to employees when they check out from the benefits enrollment experience in Employee self-service.</span></span> |
   | <span data-ttu-id="79e8e-112">**เท็มเพลตอีเมลการยืนยัน**</span><span class="sxs-lookup"><span data-stu-id="79e8e-112">**Confirmation email template**</span></span> | <span data-ttu-id="79e8e-113">เลือกเท็มเพลตอีเมลขององค์กรที่จะใช้ เมื่อส่งการยืนยันการลงทะเบียน</span><span class="sxs-lookup"><span data-stu-id="79e8e-113">Select the organization email template to use when sending the enrollment confirmation.</span></span> <span data-ttu-id="79e8e-114">ถ้าคุณไม่เลือกเท็มเพลต จะมีการส่งอีเมลทั่วไปต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="79e8e-114">If you don't select a template, the following generic email will be sent:</span></span><br><br><span data-ttu-id="79e8e-115">%EmployeeFirstName%,</span><span class="sxs-lookup"><span data-stu-id="79e8e-115">%EmployeeFirstName%,</span></span><br><br><span data-ttu-id="79e8e-116">ขอแสดงความยินดี</span><span class="sxs-lookup"><span data-stu-id="79e8e-116">Congratulations!</span></span> <span data-ttu-id="79e8e-117">คุณได้ทำการลงทะเบียนสวัสดิการเสร็จเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="79e8e-117">You’ve successfully completed benefits enrollment.</span></span><br><br><span data-ttu-id="79e8e-118">ขอบคุณ</span><span class="sxs-lookup"><span data-stu-id="79e8e-118">Thank you,</span></span><br><span data-ttu-id="79e8e-119"><Company/Org name> สวัสดิการ</span><span class="sxs-lookup"><span data-stu-id="79e8e-119"><Company/Org name> Benefits.</span></span> |
   | <span data-ttu-id="79e8e-120">**ที่อยู่อีเมลผู้ส่งเริ่มต้น**</span><span class="sxs-lookup"><span data-stu-id="79e8e-120">**Default email sender address**</span></span> | <span data-ttu-id="79e8e-121">ที่อยู่อีเมลที่จะใช้เมื่อส่งอีเมลยืนยัน</span><span class="sxs-lookup"><span data-stu-id="79e8e-121">The email address to use when sending the confirmation email.</span></span> |

3. <span data-ttu-id="79e8e-122">เลือก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="79e8e-122">Select **Save**.</span></span>