---
title: เพิ่มฟิลด์ข้อมูลในการตั้งค่าคอนฟิกภาษี
description: หัวข้อนี้อธิบายวิธีการกําหนดการตั้งค่าคอนฟิกภาษีเองโดยการเพิ่มฟิลด์ข้อมูล
author: kailiang
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 197a2d1605dd39188841aba02a71d228c7138c54
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921200"
---
# <a name="add-data-fields-in-tax-configurations"></a><span data-ttu-id="02d9e-103">เพิ่มฟิลด์ข้อมูลในการตั้งค่าคอนฟิกภาษี</span><span class="sxs-lookup"><span data-stu-id="02d9e-103">Add data fields in tax configurations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="02d9e-104">หัวข้อนี้อธิบายวิธีการเลือกกำหนดการตั้งค่าคอนฟิกภาษีโดยใช้ [ฟิลด์ข้อมูลที่เพิ่มในการรวมภาษี](tax-service-add-data-fields-tax-integration-by-extension.md)</span><span class="sxs-lookup"><span data-stu-id="02d9e-104">This topic explains how to customize tax configurations by using [data fields that are added in the tax integration](tax-service-add-data-fields-tax-integration-by-extension.md).</span></span>

## <a name="customize-the-tax-data-model"></a><span data-ttu-id="02d9e-105">เลือกกำหนดรูปแบบข้อมูลภาษี</span><span class="sxs-lookup"><span data-stu-id="02d9e-105">Customize the tax data model</span></span>

1. <span data-ttu-id="02d9e-106">ใน Microsoft Dynamics 365 Finance ไปที่ **การรายงานทางอิเล็กทรอนิกส์** \> **การตั้งค่าคอนฟิกภาษี**</span><span class="sxs-lookup"><span data-stu-id="02d9e-106">In Microsoft Dynamics 365 Finance, go to **Electronic Reporting** \> **Tax configurations**.</span></span>
2. <span data-ttu-id="02d9e-107">ในแผนภูมิการตั้งค่าคอนฟิก ให้เลือก **รูปแบบข้อมูลภาษี - ยุโรป**</span><span class="sxs-lookup"><span data-stu-id="02d9e-107">In the configuration tree, select **Tax Data Model - Europe**.</span></span> <span data-ttu-id="02d9e-108">จากนั้น ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้างการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="02d9e-108">Then, on the Action Pane, select **Create configuration**.</span></span>
3. <span data-ttu-id="02d9e-109">ในกล่องโต้ตอบแบบหล่นลง ให้เลือกตัวเลือก **แบบจำลองเอกสารต้องเสียภาษีที่สืบทอดมาจาก ชื่อ: รูปแบบข้อมูลภาษี -- ยุโรป, Microsoft** ป้อนชื่อสำหรับรูปแบบข้อมูลภาษีใหม่ แล้วจากนั้น เลือก **สร้างการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="02d9e-109">In the drop-down dialog box, select the **Taxable document model derived from Name: Tax Data Model -- Europe, Microsoft** option, enter a name for the new tax data model, and then select **Create configuration**.</span></span>
4. <span data-ttu-id="02d9e-110">เลือกรูปแบบข้อมูลภาษีที่คุณเพิ่งสร้างขึ้น และจากนั้น ในบานหน้าต่างการปฏิบัติการ ให้เลือก **ผู้ออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="02d9e-110">Select the tax data model that you just created, and then, on the Action Pane, select **Designer**.</span></span>
5. <span data-ttu-id="02d9e-111">ขยายแผนภูมิรูปแบบข้อมูล เลือก **รายการ** แล้วจากนั้น เลือก **สร้าง**</span><span class="sxs-lookup"><span data-stu-id="02d9e-111">Expand the data model tree, select **Lines**, and then select **New**.</span></span>
6. <span data-ttu-id="02d9e-112">ในกล่องโต้ตอบ **สร้างโหนด** ให้ป้อนชื่อ ระบุชนิดสินค้า แล้วจากนั้น เลือก **เพิ่ม**</span><span class="sxs-lookup"><span data-stu-id="02d9e-112">In the **Create node** dialog box, enter a name, specify the item type, and then select **Add**.</span></span>
7. <span data-ttu-id="02d9e-113">เพิ่มคอลัมน์ที่ต้องใช้ใดๆ</span><span class="sxs-lookup"><span data-stu-id="02d9e-113">Add any required columns.</span></span>
8. <span data-ttu-id="02d9e-114">ในบานหน้าต่างการดำเนินการ ให้เลือก **บันทึก** แล้วจากนั้น เลือก **ทำให้เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="02d9e-114">On the Action Pane, select **Save**, and then select **Complete**.</span></span>
9. <span data-ttu-id="02d9e-115">ปิดหน้า และดูรุ่นที่เสร็จสมบูรณ์ของรูปแบบข้อมูลภาษีของคุณ</span><span class="sxs-lookup"><span data-stu-id="02d9e-115">Close the page, and view the completed version of your tax data model.</span></span>

## <a name="customize-the-tax-configuration"></a><span data-ttu-id="02d9e-116">เลือกกำหนดการตั้งค่าคอนฟิกภาษี</span><span class="sxs-lookup"><span data-stu-id="02d9e-116">Customize the tax configuration</span></span>

1. <span data-ttu-id="02d9e-117">ใน Finance ไปที่ **การรายงานทางอิเล็กทรอนิกส์** \> **การตั้งค่าคอนฟิกภาษี**</span><span class="sxs-lookup"><span data-stu-id="02d9e-117">In Finance, go to **Electronic reporting** \> **Tax configurations**.</span></span>
2. <span data-ttu-id="02d9e-118">ในแผนภูมิการตั้งค่าคอนฟิก ให้เลือก **การตั้งค่าคอนฟิกภาษี -- ยุโรป**</span><span class="sxs-lookup"><span data-stu-id="02d9e-118">In the configuration tree, select **Tax Configuration -- Europe**.</span></span> <span data-ttu-id="02d9e-119">จากนั้น ในบานหน้าต่างการดำเนินการ ให้เลือก **สร้างการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="02d9e-119">Then, on the Action Pane, select **Create configuration**.</span></span>
3. <span data-ttu-id="02d9e-120">ในกล่องโต้ตอบแบบหล่นลง ให้เลือกตัวเลือก **การตั้งค่าคอนฟิกบริการภาษีที่สืบทอดมาจาก ชื่อ: การตั้งค่าคอนฟิกภาษี -- ยุโรป, Microsoft** ป้อนชื่อสำหรับการตั้งค่าคอนฟิกภาษีใหม่ แล้วจากนั้น เลือก **สร้างการตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="02d9e-120">In the drop-down dialog box, select the **Tax service configuration derived from Name: Tax Configuration -- Europe, Microsoft** option, enter a name for the new tax configuration, and then select **Create configuration**.</span></span>
4. <span data-ttu-id="02d9e-121">เลือกการตั้งค่าคอนฟิกภาษีที่คุณเพิ่งสร้างขึ้น และจากนั้น ในบานหน้าต่างการปฏิบัติการ ให้เลือก **ผู้ออกแบบ**</span><span class="sxs-lookup"><span data-stu-id="02d9e-121">Select the tax configuration that you just created, and then, on the Action Pane, select **Designer**.</span></span>
5. <span data-ttu-id="02d9e-122">ในส่วน **คุณสมบัติ** ในฟิลด์ **รูปแบบข้อมูล** ให้เลือกรูปแบบข้อมูลภาษีที่กำหนดเองที่คุณสร้างขึ้นก่อนหน้านี้</span><span class="sxs-lookup"><span data-stu-id="02d9e-122">In the **Properties** section, in the **Data model** field, select the customized tax data model that you created earlier.</span></span>
6. <span data-ttu-id="02d9e-123">ในฟิลด์ **รุ่นของรูปแบบข้อมูล** ให้เลือกรุ่นที่เสร็จสมบูรณ์ของรูปแบบข้อมูลภาษี</span><span class="sxs-lookup"><span data-stu-id="02d9e-123">In the **Data model version** field, select the completed version of the tax data model.</span></span>
7. <span data-ttu-id="02d9e-124">เลือก **เพิ่ม** และเพิ่มหน่วยวัดภาษีที่ต้องการ</span><span class="sxs-lookup"><span data-stu-id="02d9e-124">Select **Add**, and add the required tax measures.</span></span>
8. <span data-ttu-id="02d9e-125">ในบานหน้าต่างการดำเนินการ ให้เลือก **บันทึก** แล้วจากนั้น เลือก **ทำให้เสร็จสมบูรณ์**</span><span class="sxs-lookup"><span data-stu-id="02d9e-125">On the Action Pane, select **Save**, and then select **Complete**.</span></span>
9. <span data-ttu-id="02d9e-126">ปิดหน้า และดูรุ่นที่เสร็จสมบูรณ์ของการตั้งค่าคอนฟิกภาษีของคุณ</span><span class="sxs-lookup"><span data-stu-id="02d9e-126">Close page, and view the completed version of your tax configuration.</span></span>

## <a name="implement-tax-features-in-the-customized-tax-configuration"></a><span data-ttu-id="02d9e-127">ใช้คุณลักษณะภาษีในการตั้งค่าคอนฟิกภาษีที่กําหนดเอง</span><span class="sxs-lookup"><span data-stu-id="02d9e-127">Implement tax features in the customized tax configuration</span></span>

1. <span data-ttu-id="02d9e-128">ใน Regulatory Configuration Service (RCS) ไปยัง **คุณลักษณะที่ใช้ทั่วโลก** \> **ภาษี**</span><span class="sxs-lookup"><span data-stu-id="02d9e-128">In Regulatory Configuration Service (RCS), go to **Globalization Features** \> **Tax**.</span></span>
2. <span data-ttu-id="02d9e-129">เลือก **เพิ่ม** ป้อนข้อมูลเกี่ยวกับคุณลักษณะใหม่ แล้วจากนั้น เลือก **สร้างคุณลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="02d9e-129">Select **Add**, enter information about the new feature, and then select **Create feature**.</span></span>
3. <span data-ttu-id="02d9e-130">บนแท็บ **รุ่น** เลือกคุณลักษณะ แล้วจากนั้น เลือก **แก้ไข**</span><span class="sxs-lookup"><span data-stu-id="02d9e-130">On the **Versions** tab, select the feature, and then select **Edit**.</span></span>
4. <span data-ttu-id="02d9e-131">บนแท็บ **ทั่วไป** ในฟิลด์ **รุ่นของการตั้งค่าคอนฟิก** ให้เลือกการตั้งค่าคอนฟิกภาษีและรุ่นที่กําหนดเอง</span><span class="sxs-lookup"><span data-stu-id="02d9e-131">On the **General** tab, in the **Configuration version** field, select the customized tax configuration and version.</span></span>
5. <span data-ttu-id="02d9e-132">ในกล่องโต้ตอบ **จัดการคอลัมน์** ให้เลือกคอลัมน์ส่วนหัวและคอลัมน์รายการที่คุณต้องการรวมไว้ในหน่วยวัดภาษีที่กําหนดเองของคุณ แล้วจากนั้น เลือกปุ่มลูกศรขวาเพื่อเพิ่มในรายการ **คอลัมน์ที่เลือก**</span><span class="sxs-lookup"><span data-stu-id="02d9e-132">In the **Manage columns** dialog box, select the header and line columns that you want to include in your customized tax measure, and then select the right arrow button to add them to the **Selected columns** list.</span></span>
