---
title: ลำดับงานข้อตกลงการจัดการเงินคืน
description: หัวข้อนี้อธิบายวิธีการตั้งค่าลำดับงานข้อตกลงการจัดการเงินคืนในการอนุมัติและเรียกใช้ข้อตกลง
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: ee342de6d069131e230120c5d65aef58da8e632a
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020398"
---
# <a name="rebate-management-deal-workflows"></a><span data-ttu-id="411cb-103">ลำดับงานข้อตกลงการจัดการเงินคืน</span><span class="sxs-lookup"><span data-stu-id="411cb-103">Rebate management deal workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="411cb-104">หากต้องการอนุมัติข้อตกลงเงินคืน การจัดการเงินคืนจะใช้แพลตฟอร์มลำดับงานเดียวกันกับแอป Finance and Operations อื่นๆ</span><span class="sxs-lookup"><span data-stu-id="411cb-104">To approve rebate deals, Rebate management uses the same workflow platform as other Finance and Operations apps.</span></span> <span data-ttu-id="411cb-105">กระบวนการงานสองกระบวนการจะสัมพันธ์กับทุกลำดับงาน:</span><span class="sxs-lookup"><span data-stu-id="411cb-105">Two job processes are associated with every workflow:</span></span>

- <span data-ttu-id="411cb-106">องค์ประกอบหนึ่งของลำดับงานเรียกใช้งานข้อตกลงเพื่อให้ผู้ใช้หรือกระบวนการลำดับงานสามารถอนุมัติธุรกรรมได้</span><span class="sxs-lookup"><span data-stu-id="411cb-106">One element of the workflow activates the deal so that the user or workflow process can approve the transactions.</span></span>
- <span data-ttu-id="411cb-107">องค์ประกอบหนึ่งของลำดับงานจะอนุมัติข้อตกลงนี้</span><span class="sxs-lookup"><span data-stu-id="411cb-107">One element of the workflow approves the deal.</span></span>

<span data-ttu-id="411cb-108">ก่อนที่คุณจะสามารถใช้ข้อตกลงเงินคืนได้ นั้นจะต้องใช้งานอยู่ในโมดูล **การจัดการเงินคืน**</span><span class="sxs-lookup"><span data-stu-id="411cb-108">Before you can use a rebate deal, it must be active in the **Rebate management** module.</span></span> <span data-ttu-id="411cb-109">เมื่อต้องการเรียกใช้ข้อตกลง คุณต้องสร้างและตั้งค่าคอนฟิก *ลำดับงานข้อตกลงการจัดการเงินคืน*</span><span class="sxs-lookup"><span data-stu-id="411cb-109">To activate a deal, you must first create and configure a *Rebate management deal workflow*.</span></span>

<span data-ttu-id="411cb-110">หลังจากมีการเปิดใช้งานลำดับงานเพื่อการจัดการเงินคืนแล้ว ผู้ใช้ไม่สามารถอนุมัติข้อตกลงด้วยตนเองได้</span><span class="sxs-lookup"><span data-stu-id="411cb-110">After a workflow is activated for Rebate management, users can't manually approve deals.</span></span> <span data-ttu-id="411cb-111">ต้องใช้ลำดับงานเสมอ</span><span class="sxs-lookup"><span data-stu-id="411cb-111">The workflow must be always used.</span></span>

## <a name="create-and-manage-rebate-management-deal-workflows"></a><span data-ttu-id="411cb-112">สร้างและจัดการลำดับงานข้อตกลงการจัดการเงินคืน</span><span class="sxs-lookup"><span data-stu-id="411cb-112">Create and manage Rebate management deal workflows</span></span>

<span data-ttu-id="411cb-113">เมื่อต้องการใช้งานลำดับงานข้อตกลงการจัดการเงินคืนของคุณ ให้ไปที่ **การจัดการเงินคืน \> การตั้งค่า \> ลำดับงานการจัดการเงินคืน**</span><span class="sxs-lookup"><span data-stu-id="411cb-113">To work with your Rebate management deal workflows, go to **Rebate management \> Setup \> Rebate management workflows**.</span></span> <span data-ttu-id="411cb-114">คุณสามารถดู สร้าง และอัพเดตลำดับงานได้ตามต้องการ</span><span class="sxs-lookup"><span data-stu-id="411cb-114">There, you can view, create, and update workflows as required.</span></span> <span data-ttu-id="411cb-115">สามารถใช้งานได้ครั้งละหนึ่งลำดับงานของชนิดนี้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="411cb-115">Only one workflow of this type can be active at a time.</span></span> <span data-ttu-id="411cb-116">หากต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับลำดับงาน วิธีใช้งานกับหน้า **ลำดับงานการจัดการเงินคืน** และวิธีสร้างลำดับงาน ดูที่ [ภาพรวมระบบของลำดับงาน](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md)</span><span class="sxs-lookup"><span data-stu-id="411cb-116">For more information about workflows, how to work with the **Rebate management workflows** page, and how to create workflows, see [Workflow system overview](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) and its related topics.</span></span>

## <a name="use-a-workflow-to-activate-a-deal"></a><span data-ttu-id="411cb-117">ใช้ลำดับงานเพื่อเรียกใช้งานข้อตกลง</span><span class="sxs-lookup"><span data-stu-id="411cb-117">Use a workflow to activate a deal</span></span>

<span data-ttu-id="411cb-118">เมื่อต้องการเรียกใช้ข้อตกลงผ่านลำดับงาน ให้เปิดข้อตกลง (ตัวอย่างเช่น บนหน้า **ข้อตกลงการจัดการเงินคืนทั้งหมด**)</span><span class="sxs-lookup"><span data-stu-id="411cb-118">To activate a deal through a workflow, open the deal (for example, on the **All rebate management deals** page).</span></span> <span data-ttu-id="411cb-119">จากนั้น ในบานหน้าต่างการดำเนินการ ให้เลือก **ลำดับงาน \> ส่ง**</span><span class="sxs-lookup"><span data-stu-id="411cb-119">Then, on the Action Pane, select **Workflow \> Submit**.</span></span> <span data-ttu-id="411cb-120">หลังจากประมวลผลและอนุมัติข้อตกลงใหม่ผ่านลำดับงาน ข้อตกลงนี้จะเปิดใช้งานและพร้อมใช้งาน</span><span class="sxs-lookup"><span data-stu-id="411cb-120">After the new deal has been processed and approved through the workflow, it will be active and ready to use.</span></span>

<span data-ttu-id="411cb-121">หลังจากที่เรียกใช้ข้อตกลงแล้ว คุณไม่สามารถเปลี่ยนการตั้งค่าได้</span><span class="sxs-lookup"><span data-stu-id="411cb-121">After a deal has been activated, you can't change its setup.</span></span> <span data-ttu-id="411cb-122">ถ้าคุณต้องเปลี่ยนข้อตกลงที่ใช้งานอยู่ ยกเลิกการเรียกใช้ข้อตกลง แล้วสร้างข้อตกลงใหม่</span><span class="sxs-lookup"><span data-stu-id="411cb-122">If you must change an active deal, inactivate it, and then create a new deal.</span></span> <span data-ttu-id="411cb-123">ถ้าข้อตกลงใหม่จะคล้ายกับข้อตกลงเก่า คุณสามารถสร้างข้อตกลงได้โดยการคัดลอกข้อตกลงเก่า</span><span class="sxs-lookup"><span data-stu-id="411cb-123">If the new deal will resemble the old deal, you can create it by copying the old deal.</span></span>
