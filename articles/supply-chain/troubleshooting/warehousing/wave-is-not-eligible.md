---
title: เวฟไม่มีสิทธิ์สำหรับการล้างข้อมูล
description: เวฟไม่มีสิทธิ์สำหรับการล้างข้อมูล
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWaveTable_WHSWaveProcessingDataCleanup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3e5142cf40a6c0d308e8e952bbe17e85b498826d
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924338"
---
# <a name="wave-isnt-eligible-for-cleanup"></a><span data-ttu-id="49c60-103">เวฟไม่มีสิทธิ์สำหรับการล้างข้อมูล</span><span class="sxs-lookup"><span data-stu-id="49c60-103">Wave isn't eligible for cleanup</span></span>

<span data-ttu-id="49c60-104">รหัสข้อผิดพลาด: WaveNotEligibleForCleanup</span><span class="sxs-lookup"><span data-stu-id="49c60-104">Error code: WaveNotEligibleForCleanup</span></span>

## <a name="symptoms"></a><span data-ttu-id="49c60-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="49c60-105">Symptoms</span></span>

<span data-ttu-id="49c60-106">ระบบแสดงข้อความแสดงข้อผิดพลาดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="49c60-106">The system shows the following error message:</span></span>

> <span data-ttu-id="49c60-107">เวฟ %1 ไม่มีสิทธิ์ในการล้างข้อมูล</span><span class="sxs-lookup"><span data-stu-id="49c60-107">Wave %1 is not eligible for cleanup.</span></span>

<span data-ttu-id="49c60-108">ไม่สามารถล้างข้อมูลเวฟได้</span><span class="sxs-lookup"><span data-stu-id="49c60-108">The wave data can't be cleaned up.</span></span>  

## <a name="cause"></a><span data-ttu-id="49c60-109">สาเหตุ</span><span class="sxs-lookup"><span data-stu-id="49c60-109">Cause</span></span>

<span data-ttu-id="49c60-110">เวฟมีการประมวลผลอยู่ในเวฟอยู่ในขณะนี้ ตามที่ระบุโดยเงื่อนไขอย่างใดอย่างหนึ่งต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="49c60-110">The wave is currently being processed, as indicated by one of the following conditions:</span></span>

- <span data-ttu-id="49c60-111">ตั้งค่าฟิลด์ **สถานะของเวฟ** เป็น *กำลังดำเนินการ*</span><span class="sxs-lookup"><span data-stu-id="49c60-111">The **Wave status** field is set to *Executing*.</span></span>
- <span data-ttu-id="49c60-112">เมื่อคุณเลือก **ชุดงาน** ในกลุ่ม **เวฟ** บนแท็บ **เวฟ** ของบานหน้าต่างการลงบัญชี ฟิลด์ **สถานะ** จะไม่ถูกตั้งค่าเป็น *สิ้นสุด* *ผิดพลาด* หรือ *ยกเลิก*</span><span class="sxs-lookup"><span data-stu-id="49c60-112">When you select **Batch job** in the **Wave** group on the **Wave** tab of the Action Pane, the **Status** field isn't set to *Ended*, *Error*, or *Canceled*.</span></span> <span data-ttu-id="49c60-113">ดังนั้น ชุดงานจึงถูกรันอยู่ในขณะนี้</span><span class="sxs-lookup"><span data-stu-id="49c60-113">Therefore, a batch job is currently running.</span></span>

## <a name="resolution"></a><span data-ttu-id="49c60-114">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="49c60-114">Resolution</span></span>

<span data-ttu-id="49c60-115">ในบานหน้าต่างการรัน บนแท็บ **เวฟ** ในกลุ่ม **เวฟ** เลือก **ชุดงาน** แล้วปฏิบัติตามขั้นตอนใดขั้นตอนหนึ่งต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="49c60-115">On the Action Pane, on the **Wave** tab, in the **Wave** group, select **Batch job**, and then follow one of these steps:</span></span>

- <span data-ttu-id="49c60-116">ถ้าฟิลด์ **สถานะ** ถูกตั้งเป็น *การรัน*: ในบานหน้าต่างการรัน บนแท็บ **ชุดงาน** ในกลุ่ม **ชุดงาน** ให้เลือก **ดูงาน**</span><span class="sxs-lookup"><span data-stu-id="49c60-116">If the **Status** field is set to *Executing*: On the Action Pane, on the **Batch job** tab, in the **Batch job** group, select **View tasks**.</span></span> <span data-ttu-id="49c60-117">คุณสามารถตามความคืบหน้าได้โดยการีเฟรชหน้า **ชุดงาน**</span><span class="sxs-lookup"><span data-stu-id="49c60-117">You can follow the progress by refreshing the **Batch tasks** page.</span></span>
- <span data-ttu-id="49c60-118">ถ้าฟิลด์ **สถานะ** ไม่ถูกตั้งเป็น *การรัน*: ในบานหน้าต่างการรัน บนแท็บ **ชุดงาน** ในกลุ่ม **ฟังก์ชัน** ให้เลือก **เปลี่ยนสถานะ**</span><span class="sxs-lookup"><span data-stu-id="49c60-118">If the **Status** field isn't set to *Executing*: On the Action Pane, on the **Batch job** tab, in the **Functions** group, select **Change status**.</span></span> <span data-ttu-id="49c60-119">ในฟิลด์ **เลือกสถานะใหม่** ให้เลือก *กำลังรอ*</span><span class="sxs-lookup"><span data-stu-id="49c60-119">In the **Select new status** field, select *Waiting*.</span></span> <span data-ttu-id="49c60-120">จากนั้น เลือก **ตกลง**</span><span class="sxs-lookup"><span data-stu-id="49c60-120">Then select **OK**.</span></span>
