---
title: การสร้างข้อตกลงการให้บริการ
description: หัวข้อนี้อธิบายวิธีการใช้ลักษณะการทำงานในโมดูลการจัดการงานบริการและการจัดการและการบัญชีโครงการ เพื่อสร้างข้อตกลงการให้บริการ
author: ShylaThompson
manager: AnnBe
ms.date: 02/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 68dee63f8a426aba4bb408b6052ca9d730629bee
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 11/18/2019
ms.locfileid: "2813189"
---
# <a name="create-service-agreements"></a><span data-ttu-id="ea98e-103">การสร้างข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="ea98e-103">Create service agreements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ea98e-104">หัวข้อนี้อธิบายวิธีการใช้ลักษณะการทำงานในโมดูลการจัดการงานบริการและการจัดการและการบัญชีโครงการ เพื่อสร้างข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="ea98e-104">This topic describes how to use features in the Service management and the Project management and accounting modules to create service agreements.</span></span>

## <a name="create-a-service-agreement-from-service-management"></a><span data-ttu-id="ea98e-105">สร้างข้อตกลงการให้บริการจากการจัดการบริการ</span><span class="sxs-lookup"><span data-stu-id="ea98e-105">Create a service agreement from Service management</span></span>

1. <span data-ttu-id="ea98e-106">นำทางไปยัง **การจัดการงานบริการ**</span><span class="sxs-lookup"><span data-stu-id="ea98e-106">Navigate to **Service management**.</span></span>
2. <span data-ttu-id="ea98e-107">คลิก **ข้อตกลงการให้บริการ** เพื่อสร้างรายการข้อตกลงการให้บริการใหม่ในส่วนหัวของหน้า</span><span class="sxs-lookup"><span data-stu-id="ea98e-107">Click **Service agreements** to create a new service agreement line in the page header.</span></span> 
3. <span data-ttu-id="ea98e-108">คลิก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="ea98e-108">Click **New**.</span></span> <span data-ttu-id="ea98e-109">ป้อนคำอธิบาย เลือกการอ้างอิงถึงโครงการในฟิลด์ **ID โครงการ** และกรอกข้อมูลในฟิลด์และรายการที่เหลือสำหรับข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="ea98e-109">Enter a description, select a reference to a project in the **Project ID** field, and fill in the rest of the fields and lines for the service agreement.</span></span> <span data-ttu-id="ea98e-110">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="ea98e-110">Click **Save**.</span></span>
4. <span data-ttu-id="ea98e-111">บนแท็บ **ความสัมพันธ์** เลือก **ออบเจ็กต์ที่ให้บริการ** หรือ **งานบริการ** เพื่อสร้างความสัมพันธ์ของออบเจ็กต์ที่ให้บริการ หรือความสัมพันธ์ของงานบริการสำหรับข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="ea98e-111">On the **Relations** tab, select **Service objects** or **Service tasks** to create service object relations or service task relations for the service agreement.</span></span> <span data-ttu-id="ea98e-112">วัตถุที่ให้บริการและภารกิจการให้บริการที่คุณสร้างความสัมพันธ์ให้ สามารถนำมาแนบกับบรรทัดของข้อตกลงการให้บริการได้</span><span class="sxs-lookup"><span data-stu-id="ea98e-112">The service objects and tasks that you have created relations for can be attached on the lines of the service agreement.</span></span>
5. <span data-ttu-id="ea98e-113">ในครึ่งด้านล่างของหน้า ให้สร้างรายการข้อตกลงการให้บริการโดยการคัดลอกรายการจากเท็มเพลตการบริการ ข้อตกลงการให้บริการอื่น หรือสร้างรายการข้อตกลงการให้บริการด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="ea98e-113">In the lower half of the page, create service agreement lines by copying lines from a service template, another service agreement, or manually creating the service-agreement lines.</span></span>

> [!NOTE]
> <span data-ttu-id="ea98e-114">ถ้าคุณคัดลอกรายการลงในข้อตกลงการให้บริการจากข้อตกลงการให้บริการอื่น คุณสามารถบ่งชี้ได้ว่าคุณต้องการคัดลอกความสัมพันธ์ของออบเจ็กต์ที่ให้บริการและงานบริการด้วยหรือไม่</span><span class="sxs-lookup"><span data-stu-id="ea98e-114">If you copy lines into the service agreement from another service agreement, you can indicate whether you also want to copy service object and service task relations.</span></span> <span data-ttu-id="ea98e-115">ถ้าคุณคัดลอกความสัมพันธ์เหล่านี้ ความสัมพันธ์ดังกล่าวจะมีการเพิ่มรวมกับความสัมพันธ์ที่มีอยู่แล้วบนข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="ea98e-115">If you copy these relations, they are added to any existing relations on the service agreement.</span></span> <span data-ttu-id="ea98e-116">ถ้าคุณคัดลอกบรรทัดข้อตกลงการให้บริการจากเท็มเพลตการบริการ ความสัมพันธ์ของวัตถุที่ให้บริการและความสัมพันธ์ของภารกิจการให้บริการ จะมีการคัดลอกเป็นความสัมพันธ์ของวัตถุที่ให้บริการและความสัมพันธ์ของภารกิจการให้บริการ บนบรรทัดข้อตกลงการให้บริการใหม่โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="ea98e-116">If you copy service-agreement lines from a service template, the service-object and service-task relations are automatically copied as service-object relations and service-task relations on the new service-agreement lines.</span></span>

## <a name="create-service-agreement-lines-manually"></a><span data-ttu-id="ea98e-117">สร้างรายการข้อตกลงการให้บริการด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="ea98e-117">Create service agreement lines manually</span></span>

1. <span data-ttu-id="ea98e-118">จากหน้า **ข้อตกลงการให้บริการ** เพิ่มรายการข้อตกลงการให้บริการในกริดรายการ</span><span class="sxs-lookup"><span data-stu-id="ea98e-118">From the **Service agreements** page, add a service agreement line in the lines grid.</span></span> 
2. <span data-ttu-id="ea98e-119">ป้อนข้อมูลที่เหมาะสมสำหรับรายการข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="ea98e-119">Enter the appropriate information for the service agreement line.</span></span> 
3. <span data-ttu-id="ea98e-120">กด **CTRL+S** เพื่อบันทึกรายการ และจากนั้นปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="ea98e-120">Press **CTRL+S** to save the line, and then close the page.</span></span>

## <a name="create-a-service-agreement-from-project"></a><span data-ttu-id="ea98e-121">การสร้างข้อตกลงการให้บริการจากโครงการ</span><span class="sxs-lookup"><span data-stu-id="ea98e-121">Create a service agreement from Project</span></span>

1. <span data-ttu-id="ea98e-122">คลิก **การจัดการและการบัญชีโครงการ**</span><span class="sxs-lookup"><span data-stu-id="ea98e-122">Click **Project management and accounting**.</span></span>
2. <span data-ttu-id="ea98e-123">คลิก **โครงการทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="ea98e-123">Click **All projects**.</span></span>
3. <span data-ttu-id="ea98e-124">เลือกโครงการจากรายการ</span><span class="sxs-lookup"><span data-stu-id="ea98e-124">Select the project from the list.</span></span>
4. <span data-ttu-id="ea98e-125">บน **บานหน้าต่างการดำเนินการ** คลิก **จัดการ**</span><span class="sxs-lookup"><span data-stu-id="ea98e-125">On the **Action Pane**, click **Manage**.</span></span> <span data-ttu-id="ea98e-126">ในกลุ่มการดำเนินการ **ใหม่** คลิก **บริการ** และเลือก **ข้อตกลงการให้บริการ**</span><span class="sxs-lookup"><span data-stu-id="ea98e-126">In the **New** Action group, click **Service** and select **Service agreement**.</span></span>
5. <span data-ttu-id="ea98e-127">ทำตามขั้นตอนในส่วนชื่อว่า **สร้างข้อตกลงการให้บริการ** ตามที่อธิบายไว้ก่อนหน้านี้ในหัวข้อนี้ เพื่อป้อนข้อมูลอ้างอิงโครงการ</span><span class="sxs-lookup"><span data-stu-id="ea98e-127">Follow the steps in the section titled **Create a service agreement** as described earlier in this topic to enter the project reference.</span></span>


## <a name="related-topics"></a><span data-ttu-id="ea98e-128">หัวข้อที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="ea98e-128">Related topics</span></span>

[<span data-ttu-id="ea98e-129">ภาพรวมของการพัฒนาและจัดทำข้อตกลงการให้บริการ</span><span class="sxs-lookup"><span data-stu-id="ea98e-129">Develop and establish service agreements overview</span></span>](service-agreements.md)


