---
title: ลำดับหมายเลขแบบรวมสำหรับรหัสงาน
description: ลักษณะการงานนี้แสดงลำดับหมายเลขแบบรวมหนึ่งๆ ที่สร้างรหัสงานเกี่ยวกับการควบคุมการผลิต การปฏิบัติการผลิต และโมดูลเวลาและการเข้างาน
author: johanhoffmann
ms.date: 03/25/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 00212803c46d898a39eafbc5c62016eb829535e2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824953"
---
# <a name="unified-number-sequence-for-job-ids"></a><span data-ttu-id="d62f6-103">ลำดับหมายเลขแบบรวมสำหรับรหัสงาน</span><span class="sxs-lookup"><span data-stu-id="d62f6-103">Unified number sequence for job IDs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d62f6-104">ลักษณะการงานนี้แสดงลำดับหมายเลขแบบรวมหนึ่งๆ ที่สร้างรหัสงานเกี่ยวกับการควบคุมการผลิต การปฏิบัติการผลิต และโมดูลเวลาและการเข้างาน</span><span class="sxs-lookup"><span data-stu-id="d62f6-104">This feature provides a single, unified number sequence that generates job IDs for the Production control, Manufacturing execution, and Time and attendance modules.</span></span> <span data-ttu-id="d62f6-105">ก่อนหน้านี้ คุณสามารถเลือกลำดับหมายเลขที่แตกต่างกันให้กับแต่ละโมดูลเหล่านี้ ซึ่งอาจส่งผลให้เกิดรหัสงานที่ขัดแย้งกัน ถ้าลำดับเหล่านี้สองลำดับหรือมากกว่าใช้รูปแบบที่เหมือนกัน</span><span class="sxs-lookup"><span data-stu-id="d62f6-105">Previously, you were able to choose a different number sequence for each of these modules, which could result in conflicting job IDs if two or more of these sequences used an identical format.</span></span> <span data-ttu-id="d62f6-106">ความขัดแย้งดังกล่าวอาจก่อให้เกิดความเสียหายของข้อมูลได้</span><span class="sxs-lookup"><span data-stu-id="d62f6-106">Such a conflict can cause data corruption.</span></span>

## <a name="turn-on-this-feature-for-your-system"></a><span data-ttu-id="d62f6-107">เปิดใช้งานคุณลักษณะนี้สำหรับระบบของคุณ</span><span class="sxs-lookup"><span data-stu-id="d62f6-107">Turn on this feature for your system</span></span>

<span data-ttu-id="d62f6-108">ถ้าระบบของคุณยังไม่ได้รวมคุณลักษณะที่อธิบายไว้ในหัวข้อนี้ ให้ไปที่ [การจัดการคุณลักษณะ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) และเปิดคุณลักษณะ *สำดับหมายเลขแบบรวมของรหัสงาน*</span><span class="sxs-lookup"><span data-stu-id="d62f6-108">If your system doesn't already include the feature described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the *Unified number sequence for job IDs* feature.</span></span>

## <a name="set-up-the-unified-number-sequence-for-job-ids"></a><span data-ttu-id="d62f6-109">ตั้งค่าสำดับหมายเลขแบบรวมของรหัสงาน</span><span class="sxs-lookup"><span data-stu-id="d62f6-109">Set up the unified number sequence for job IDs</span></span>

<span data-ttu-id="d62f6-110">หลังจากเปิดใช้งานคุณลักษณะนี้ การตั้งค่าลำดับหมายเลข **รหัสงาน** ที่มีอยู่ ซึ่งอยู่ในหน้าพารามิเตอร์ของโมดูลการควบคุมการผลิต การปฏิบัติการผลิต และโมดูลเวลาและการเข้างานจะถูกไม่สนับสนุน และฟิลด์ **รหัสงานรวม** ใหม่จะถูกเพิ่ม</span><span class="sxs-lookup"><span data-stu-id="d62f6-110">After enabling this feature, the existing **Job identification** number-sequence settings located on the parameters pages for the Production control, Manufacturing execution, and Time and attendance modules will be deprecated and a new **Unified job ID** field will be added.</span></span> <span data-ttu-id="d62f6-111">ค่า **รหัสงานแบบรวม** จะถูกใช้ร่วมกันโดยโมดูลทั้งสามโมดูล ดังนั้นจึงตรวจสอบให้แน่ใจว่าโมดูลทั้งหมดอ้างอิงลำดับหมายเลขเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="d62f6-111">The **Unified job ID** value is shared by all three modules, thus ensuring that all modules reference the same number sequence.</span></span> <span data-ttu-id="d62f6-112">รหัสงานจะไม่มีเอกลักษณ์เฉพาะระหว่างโมดูลทั้งสามโมดูลและจะไม่มีความขัดแย้งเกิดขึ้น</span><span class="sxs-lookup"><span data-stu-id="d62f6-112">Job IDs will therefore be unique across all three modules and a conflict will never occur.</span></span>

<span data-ttu-id="d62f6-113">หากต้องการตั้งค่าสำดับหมายเลขแบบรวมของรหัสงาน:</span><span class="sxs-lookup"><span data-stu-id="d62f6-113">To set up the unified number sequence for job IDs:</span></span>

1. <span data-ttu-id="d62f6-114">เปิดลักษณะการงานตามที่อธิบายไว้ในส่วนก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="d62f6-114">Turn on the feature as described in the previous section.</span></span>
1. <span data-ttu-id="d62f6-115">ระบุลำดับหมายเลขที่คุณต้องการใช้กับรหัสงานแบบรวมของคุณ หรือสร้างรหัสใหม่</span><span class="sxs-lookup"><span data-stu-id="d62f6-115">Either identify the number sequence you want to use for your unified job IDs, or create a new one.</span></span> <span data-ttu-id="d62f6-116">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ภาพรวมของลำดับหมายเลข](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md)</span><span class="sxs-lookup"><span data-stu-id="d62f6-116">For more information, see [Number sequences overview](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).</span></span>
1. <span data-ttu-id="d62f6-117">ไปที่พารามิเตอร์ **พารามิเตอร์การควบคุมการผลิต** **การเริ่มการผลิต** หรือหน้า **พารามิเตอร์เวลาและการเข้างาน**</span><span class="sxs-lookup"><span data-stu-id="d62f6-117">Go to the **Production control parameters**, **Manufacturing execution parameters**, or **Time and attendance parameters** page.</span></span> <span data-ttu-id="d62f6-118">ไม่ว่าคุณจะเลือกหน้าใดเนื่องจากเมื่อคุณตั้งค่านี้บนหน้าหน้าใดๆ หน้าอื่นๆ ทั้งหมดจะอัพเดตโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="d62f6-118">It doesn't matter which one you choose because when you make this setting on any of those pages, all of the other pages will update automatically.</span></span>
1. <span data-ttu-id="d62f6-119">เปิดแท็บ **ลำดับหมายเลข** ในหน้าพารามิเตอร์ที่คุณเลือก</span><span class="sxs-lookup"><span data-stu-id="d62f6-119">Open the **Number sequences** tab on your selected parameters page.</span></span>
1. <span data-ttu-id="d62f6-120">กําหนด **รหัสลำดับหมายเลข** ที่คุณได้ระบุก่อนหน้านี้ให้กับแถว **รหัสงานรวมของกริด**</span><span class="sxs-lookup"><span data-stu-id="d62f6-120">Assign the **Number sequence code** that you identified previously to the **Unified job IDs** row of the grid.</span></span>
