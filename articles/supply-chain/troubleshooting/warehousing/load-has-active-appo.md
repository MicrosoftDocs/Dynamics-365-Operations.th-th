---
title: คุณไม่สามารถยืนยันการจัดส่งได้ เนื่องจากปัญหากับปฏิทิน
description: คุณไม่สามารถยืนยันการจัดส่งได้ เนื่องจากปัญหากับปฏิทิน
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f1fccd10d8867252f32b37c77f9a3bad54157bdd
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938562"
---
# <a name="you-cant-confirm-a-shipment-because-of-an-issue-with-the-calendar"></a><span data-ttu-id="74434-103">คุณไม่สามารถยืนยันการจัดส่งได้ เนื่องจากปัญหากับปฏิทิน</span><span class="sxs-lookup"><span data-stu-id="74434-103">You can't confirm a shipment because of an issue with the calendar</span></span>

<span data-ttu-id="74434-104">รหัสข้อผิดพลาด: TRX2716</span><span class="sxs-lookup"><span data-stu-id="74434-104">Error code: TRX2716</span></span>

## <a name="symptoms"></a><span data-ttu-id="74434-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="74434-105">Symptoms</span></span>

<span data-ttu-id="74434-106">เมื่อคุณพยายามยืนยันการจัดส่ง ระบบจะแสดงข้อความแสดงข้อผิดพลาดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="74434-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="74434-107">ชนิดปฏิทิน %1 กำหนดให้ต้องมีการเช็คอินและเช็คเอาท์การนัดหมาย %2</span><span class="sxs-lookup"><span data-stu-id="74434-107">The calendar type %1 requires the appointment %2 to be checked in and out.</span></span>

<span data-ttu-id="74434-108">ดังนั้นคุณจึงไม่สามารถยืนยันการจัดส่งของสินค้าได้</span><span class="sxs-lookup"><span data-stu-id="74434-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="74434-109">สาเหตุ</span><span class="sxs-lookup"><span data-stu-id="74434-109">Cause</span></span>

<span data-ttu-id="74434-110">มีการนัดหมายที่ใช้งานอยู่</span><span class="sxs-lookup"><span data-stu-id="74434-110">Active appointments for the load exist.</span></span> <span data-ttu-id="74434-111">ตัวอย่างเช่น มีกฎที่ต้องมีการเช็คอินโดยพนักงานขับรถ</span><span class="sxs-lookup"><span data-stu-id="74434-111">For example, there is a rule that requires driver check-in.</span></span> <span data-ttu-id="74434-112">ขณะนี้โหลดอยู่ในสถานะที่การยืนยันการจัดส่งล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="74434-112">Therefore, the load is currently in a state where shipment confirmation fails.</span></span>

## <a name="resolution"></a><span data-ttu-id="74434-113">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="74434-113">Resolution</span></span>

<span data-ttu-id="74434-114">คุณต้องตรวจสอบและแก้ไขปัญหาใด ๆ กับการนัดหมายที่ใช้งานอยู่ที่เชื่อมโยงกับงาน</span><span class="sxs-lookup"><span data-stu-id="74434-114">You must investigate and fix any issues with the active appointments that are linked to the load.</span></span>

1. <span data-ttu-id="74434-115">ไปที่ **การจัดการคลังสินค้า \> จำนวนงานในศูนย์การผลิต \> จำนวนงานในศูนย์การผลิตทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="74434-115">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="74434-116">เลือกสินค้าที่การจัดส่งไม่สามารถยืนยันได้</span><span class="sxs-lookup"><span data-stu-id="74434-116">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="74434-117">บนบานหน้าต่างการดำเนินการ บนแท็บ **การขนส่ง** ในกลุ่ม **การนัดหมาย** ให้เลือก **การจัดกำหนดการนัดหมาย**</span><span class="sxs-lookup"><span data-stu-id="74434-117">On the Action Pane, on the **Transportation** tab, in the **Appointments** group, select **Appointment scheduling**.</span></span>
1. <span data-ttu-id="74434-118">ทำตามขั้นตอนเหล่านี้</span><span class="sxs-lookup"><span data-stu-id="74434-118">Follow one of these steps:</span></span>

    - <span data-ttu-id="74434-119">ตรวจสอบให้แน่ใจว่าการเช็คอิน/เช็คเอาท์พนักงานขับรถเสร็จสิ้นแล้วสำหรับการนัดหมาย</span><span class="sxs-lookup"><span data-stu-id="74434-119">Make sure that driver check-in/check-out is completed for the appointment.</span></span>
    - <span data-ttu-id="74434-120">ทำให้เสร็จสมบูรณ์หรือยกเลิกการนัดหมาย</span><span class="sxs-lookup"><span data-stu-id="74434-120">Complete or cancel the appointment.</span></span>
    - <span data-ttu-id="74434-121">ปิดใช้งานตัวเลือก **ต้องใช้การเช็คอินโดยพนักงานขับรถ** สำหรับกฎการนัดหมายที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="74434-121">Disable the **Driver check-in required** option for the related appointment rule.</span></span>
