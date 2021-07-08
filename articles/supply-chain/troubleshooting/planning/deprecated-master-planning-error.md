---
title: คุณจะได้รับข้อผิดพลาดเมื่อรันกลไกจัดการการวางแผนหลักในตัว
description: เมื่อคุณรันกลไกจัดการการวางแผนหลักในตัวที่เลิกใช้งาน คุณจะได้รับข้อผิดพลาด
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: Dialog_ReqCalcScheduleItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9c950292a4f43319d21a7deafdfb341b7bef15d8
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294192"
---
# <a name="you-receive-an-error-when-running-the-built-in-master-planning-engine"></a><span data-ttu-id="d8072-103">คุณจะได้รับข้อผิดพลาดเมื่อรันกลไกจัดการการวางแผนหลักในตัว</span><span class="sxs-lookup"><span data-stu-id="d8072-103">You receive an error when running the built-in master planning engine</span></span>

<span data-ttu-id="d8072-104">รหัสข้อผิดพลาด: ReqCalcScheduleItemTablePlanningOptimizationFitError</span><span class="sxs-lookup"><span data-stu-id="d8072-104">Error code: ReqCalcScheduleItemTablePlanningOptimizationFitError</span></span>

## <a name="symptoms"></a><span data-ttu-id="d8072-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="d8072-105">Symptoms</span></span>

<span data-ttu-id="d8072-106">เมื่อคุณรันการวางแผนหลักโดยใช้กลไกจัดการการวางแผนหลักในตัวที่เลิกใช้งาน คุณจะได้รับข้อผิดพลาดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="d8072-106">When you run master planning by using the deprecated built-in master planning engine, you receive the following error message:</span></span>

> <span data-ttu-id="d8072-107">คุณได้รับข้อความแสดงข้อความแสดงข้อผิดพลาดนี้เนื่องจากมีการใช้กลไกจัดการการวางแผนหลักในตัวสำหรับสถานการณ์จำลองที่สนับสนุนโดยการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="d8072-107">You receive this error message because the built-in master planning engine was used for scenarios supported by Planning Optimization.</span></span> <span data-ttu-id="d8072-108">คุณควรโยกย้ายเพื่อเพิ่มประสิทธิภาพการวางแผนในขณะนี้ เนื่องจากการวางแผนหลักที่มีอยู่แล้วภายในปัจจุบันจะไม่ได้รับการสนับสนุน</span><span class="sxs-lookup"><span data-stu-id="d8072-108">You should migrate to Planning Optimization now, as the current built-in master planning will be deprecated.</span></span> <span data-ttu-id="d8072-109">โปรดทราบว่าการวางแผนหลักนี้ทำงานเสร็จเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="d8072-109">Note that this master planning run did complete successfully.</span></span> <span data-ttu-id="d8072-110">ในกรณีที่การโยกย้ายของคุณมีความสัมพันธ์อย่างแข็งแรงในลักษณะการทำงานที่ค้างอยู่ ข้อยกเว้นในการใช้งานของกลไกจัดการการวางแผนหลักในตัวต่อสามารถร้องขอได้</span><span class="sxs-lookup"><span data-stu-id="d8072-110">In case your migration has strong dependencies on pending features, an exception to continued usage of the built-in master planning engine can be requested.</span></span> <span data-ttu-id="d8072-111">โปรดกรอกแบบสอบถามต่อไปนี้ให้ครบถ้วนเพื่อเริ่มต้นใช้งานและถ้าข้อยกเว้นของคำขอเกี่ยวข้องจากการโยกย้ายไปยังการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="d8072-111">Please complete the following questionnaire to get started and, if relevant, request an exception from migration to Planning Optimization.</span></span> [<span data-ttu-id="d8072-112">แบบสอบถามการย้ายและการเพิ่มประสิทธิภาพการวางแผนและข้อยกเว้น</span><span class="sxs-lookup"><span data-stu-id="d8072-112">Planning Optimization migration and exception questionnaire</span></span>](https://go.microsoft.com/fwlink/?linkid=2144962)

## <a name="cause"></a><span data-ttu-id="d8072-113">สาเหตุ</span><span class="sxs-lookup"><span data-stu-id="d8072-113">Cause</span></span>

<span data-ttu-id="d8072-114">ถ้าคุณรันการวางแผนและไม่ใช้คุณลักษณะการควบคุมการผลิต คุณควรพิจารณาย้ายไปยังการเพิ่มประสิทธิภาพการวางแผน</span><span class="sxs-lookup"><span data-stu-id="d8072-114">If you run planning and don't use production control features, you should consider migrating to Planning Optimization.</span></span> <span data-ttu-id="d8072-115">กลไกจัดการการวางแผนหลักในตัวเลิกใช้แล้ว</span><span class="sxs-lookup"><span data-stu-id="d8072-115">The built-in master planning engine is being deprecated.</span></span> <span data-ttu-id="d8072-116">ดังนั้น ถ้าคุณต้องการใช้ต่อโดยไม่ได้รับข้อความแสดงข้อผิดพลาด คุณต้องใช้ข้อยกเว้นจาก Microsoft</span><span class="sxs-lookup"><span data-stu-id="d8072-116">Therefore, if you want to continue to use it without receiving the error message, you must apply for an exception from Microsoft.</span></span>

## <a name="resolution"></a><span data-ttu-id="d8072-117">การแก้ปัญหา</span><span class="sxs-lookup"><span data-stu-id="d8072-117">Resolution</span></span>

<span data-ttu-id="d8072-118">หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับวิธีการย้ายไปยังการเพิ่มประสิทธิภาพการวางแผน หรือวิธีการใช้ข้อยกเว้น เพื่อให้คุณสามารถใช้งานกลไกจัดการการวางแผนในตัวที่ไม่สนับสนุนต่อไปได้ โปรดดูที่ [การย้ายไปยังการเพิ่มประสิทธิภาพการวางแผนเพื่อการวางแผนหลัก](/dynamics365/supply-chain/master-planning/new-master-planning-engine)</span><span class="sxs-lookup"><span data-stu-id="d8072-118">For more information about how to migrate to Planning Optimization, or how to apply for an exception so that you can continue to use the deprecated built-in planning engine instead, see [Migration to Planning Optimization for master planning](/dynamics365/supply-chain/master-planning/new-master-planning-engine).</span></span>
