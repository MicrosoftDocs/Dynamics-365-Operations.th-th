---
title: สร้างแบบจำลองการคาดการณ์สำหรับงบประมาณโครงการ
description: หัวข้อนี้อธิบายเกี่ยวกับวิธีการสร้างแบบจำลองการคาดการณ์สำหรับงบประมาณคงเหลือ
author: RadhikaRS
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 07e540f23a668b40a54906a67d87552fe991825a
ms.sourcegitcommit: 5de75c61c33e57c813944f1ab6100aceb020d432
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/29/2020
ms.locfileid: "3321790"
---
# <a name="create-forecast-models-for-project-budgets"></a><span data-ttu-id="99db7-103">สร้างแบบจำลองการคาดการณ์สำหรับงบประมาณโครงการ</span><span class="sxs-lookup"><span data-stu-id="99db7-103">Create forecast models for project budgets</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="99db7-104">หัวข้อนี้อธิบายเกี่ยวกับวิธีการสร้างแบบจำลองการคาดการณ์สำหรับงบประมาณคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="99db7-104">This topic describes how to create a forecast model for remaining budgets.</span></span> <span data-ttu-id="99db7-105">โครงการที่อยู่ภายใต้การควบคุมงบประมาณจะใช้งบประมาณสองชนิด ได้แก่ งบประมาณเดิม และงบประมาณคงเหลือ</span><span class="sxs-lookup"><span data-stu-id="99db7-105">A project that is subject to budget control uses two types of budgets: original and remaining.</span></span> <span data-ttu-id="99db7-106">เมื่อคุณสร้างงบประมาณโครงการ คุณต้องระบุข้อมูลแบบจำลองการคาดการณ์งบประมาณเดิมและคงเหลือที่สร้างขึ้นในหน้า **แบบจำลองการคาดการณ์**</span><span class="sxs-lookup"><span data-stu-id="99db7-106">When you create a project budget, you must specify the original and remaining budget forecast models that were created in the **Forecast models** page.</span></span> <span data-ttu-id="99db7-107">งบประมาณโครงการตามแบบจำลองที่ระบุจะถูกสร้างเมื่อคุณยืนยันงบประมาณโครงการ</span><span class="sxs-lookup"><span data-stu-id="99db7-107">Project budgets based on the specified models are created when you commit the project budget.</span></span>

> [!NOTE]
> <span data-ttu-id="99db7-108">แบบจำลองการคาดการณ์ที่ใช้สำหรับการควบคุมงบประมาณไม่สามารถมีแบบจำลองย่อย หรือไม่สามารถใช้เป็นแบบจำลองย่อย</span><span class="sxs-lookup"><span data-stu-id="99db7-108">A forecast model that is used for budget control can’t have a submodel or be used as a submodel.</span></span>

1. <span data-ttu-id="99db7-109">เลือก **การจัดการและการบัญชีโครงการ** > **การตั้งค่า** > **การคาดการณ์**  > **แบบจำลองการคาดการณ์**</span><span class="sxs-lookup"><span data-stu-id="99db7-109">Select **Project management and accounting** > **Setup** > **Forecasts**  > **Forecast models**.</span></span>
2. <span data-ttu-id="99db7-110">เลือก **สร้าง** เพื่อสร้างแบบจำลองการคาดการณ์ใหม่ จากนั้นป้อนหมายเลขรหัสรุ่นและชื่อสำหรับแบบจำลองใหม่</span><span class="sxs-lookup"><span data-stu-id="99db7-110">Select **New** to create a new forecast model, and then enter a model ID number and name for the new model.</span></span> 
3. <span data-ttu-id="99db7-111">ตั้งค่าตัวเลือก **หยุด** เป็น **ใช่** เพื่อป้องกันไม่ให้มีการเปลี่ยนแปลงใดๆ กับบรรทัดการคาดการณ์สำหรับแบบจำลองการคาดการณ์</span><span class="sxs-lookup"><span data-stu-id="99db7-111">Set the **Stopped** option to **Yes** to prevent any changes to the forecast lines for the forecast model.</span></span> 
4. <span data-ttu-id="99db7-112">ถ้ารายการการคาดการณ์ที่แบบจำลองเชื่อมโยงอยู่ควรสร้างการคาดการณ์กระแสเงินสดในบัญชีแยกประเภททั่วไป ตั้งค่า **รวมการคาดการณ์กระแสเงินสด** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="99db7-112">If the forecast lines that the model is associated with should generate cash flow forecasts in the general ledger, set **Include in Cash flow forecasts** to **Yes.**</span></span> 
5. <span data-ttu-id="99db7-113">เมื่อต้องการใช้วันที่โครงการเป็นวันที่ในใบแจ้งหนี้ ให้กำหนด **วันที่ในใบแจ้งหนี้การคาดการณ์** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="99db7-113">To use the project date as the invoice date, set **Forecast Invoice date** to **Yes**.</span></span> 
6. <span data-ttu-id="99db7-114">ในฟิลด์ **ชนิดงบประมาณ** เลือกชนิดแบบจำลองชนิดใดชนิดหนึ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="99db7-114">In the **Budget type** field, select one of the following model types:</span></span>

   - <span data-ttu-id="99db7-115">**งบประมาณเดิม**: ใช้แบบจำลองชนิดนี้สำหรับยอดเงินงบประมาณเดิมที่มีการยืนยันเมื่อสร้างและอนุมัติงบประมาณเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="99db7-115">**Original budget**: Use the original budget amounts that are committed when the initial budget is created and approved.</span></span>
   - <span data-ttu-id="99db7-116">**งบประมาณคงเหลือ**: ใช้แบบจำลองชนิดนี้สำหรับยอดเงินงบประมาณคงเหลือในระหว่างอายุของโครงการ</span><span class="sxs-lookup"><span data-stu-id="99db7-116">**Remaining budget**: Use the remaining budget amounts during the life of the project.</span></span> <span data-ttu-id="99db7-117">ยอดดุลในแบบจำลองการคาดการณ์นี้จะลดลงโดยธุรกรรมที่เกิดขึ้นจริง และเพิ่มหรือลดลงโดยการปรับปรุงงบประมาณ</span><span class="sxs-lookup"><span data-stu-id="99db7-117">The balances in this forecast model are reduced by actual transactions and increased or decreased by budget revisions.</span></span>
   - <span data-ttu-id="99db7-118">**งบประมาณยกไป**: ใช้ยอดเงินงบประมาณยกไปสำหรับโครงการ</span><span class="sxs-lookup"><span data-stu-id="99db7-118">**Carry-forward**: Use the carry-forward budget amounts for the project.</span></span> <span data-ttu-id="99db7-119">การยกยอดไปเป็นกระบวนการเสริมที่สามารถเรียกใช้เพื่อโอนย้ายยอดเงินงบประมาณที่ไม่ได้ใช้จากปีบัญชีหนึ่งไปยังอีกปีบัญชีหนึ่ง</span><span class="sxs-lookup"><span data-stu-id="99db7-119">Carry-forward is an optional process that can be run to transfer unused budget amounts from one fiscal year to another.</span></span>

7. <span data-ttu-id="99db7-120">ตั้งค่าตัวเลือกต่อไปนี้ตามต้องการ:</span><span class="sxs-lookup"><span data-stu-id="99db7-120">Set the following options as required:</span></span>

   - <span data-ttu-id="99db7-121">เปิดใช้งาน **วันที่ในใบแจ้งหนี้การคาดการณ์** เพื่อใช้วันที่โครงการเป็นวันที่ในใบแจ้งหนี้</span><span class="sxs-lookup"><span data-stu-id="99db7-121">Enable **Forecast invoice date** to use the project date as the invoice date.</span></span>
   - <span data-ttu-id="99db7-122">เปิดใช้งาน **การคาดการณ์กับ WIP** เพื่อคาดการณ์ตามงานระหว่างดำเนินการ (WIP) แล้วเลือกชนิดของ WIP</span><span class="sxs-lookup"><span data-stu-id="99db7-122">Enable **Forecast with WIP** to forecast based on work in progress (WIP), and then select the type of WIP.</span></span> 
   - <span data-ttu-id="99db7-123">คุณสามารถเก็บ **ชนิดงบประมาณ** เริ่มต้นเป็น **ไม่มี** หรือป้อนชนิดใหม่ก็ได้</span><span class="sxs-lookup"><span data-stu-id="99db7-123">You can keep the default **Budget type** as **None** or enter a new type.</span></span> <span data-ttu-id="99db7-124">ชนิดงบประมาณไม่สามารถเปลี่ยนได้ หลังจากที่คุณเปลี่ยนเรกคอร์ด</span><span class="sxs-lookup"><span data-stu-id="99db7-124">The budget type can't be changed after you change a record.</span></span>     
    > [!NOTE]
    > <span data-ttu-id="99db7-125">ถ้าคุณเปลี่ยนชนิดงบประมาณเริ่มต้น ตัวเลือกอื่นๆ ทั้งหมดจะไม่พร้อมใช้งานสำหรับการอัพเดต และคุณไม่สามารถนำแบบจำลองการคาดการณ์นี้มาใช้ใหม่ได้</span><span class="sxs-lookup"><span data-stu-id="99db7-125">If you change the default budget type, all other options will become unavailable for updates, and you can't reuse this forecast model.</span></span> 
   


 

