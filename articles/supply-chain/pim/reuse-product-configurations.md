---
title: "นำการจัดโครงแบบผลิตภัณฑ์มาใช้ใหม่"
description: "คุณสามารถระบุว่าคุณต้องการนำการตั้งค่าคอนฟิกที่มีอยู่กลับมาใช้ใหม่โดยอัตโนมัติสำหรับผลิตภัณฑ์ จากนั้น เมื่อผู้ใช้ดำเนินการรอบเวลาการตั้งค่าคอนฟิกเสร็จสมบูรณ์แล้ว ระบบจะตรวจสอบว่ามีการตั้งค่าคอนฟิกที่สอดคล้องกับการเลือกของผู้ใช้อยู่แล้วหรือไม่ ถ้าพบการตั้งค่าคอนฟิกที่ตรงกัน รหัสการตั้งค่าคอนฟิก ใบตราส่ง (BOM) ที่สอดคล้องกัน และกระบวนการผลิตจะถูกนำกลับมาใช้ใหม่"
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 201813
ms.assetid: 4985e308-7824-41fc-83fd-fd0bdae888e3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: dd703d5c0d35b592ebd1b8fda80e0eeed4185ce1
ms.contentlocale: th-th
ms.lasthandoff: 05/08/2018

---

# <a name="reuse-product-configurations"></a><span data-ttu-id="4ac16-105">นำการจัดโครงแบบผลิตภัณฑ์มาใช้ใหม่</span><span class="sxs-lookup"><span data-stu-id="4ac16-105">Reuse product configurations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4ac16-106">คุณสามารถระบุว่าคุณต้องการนำการตั้งค่าคอนฟิกที่มีอยู่กลับมาใช้ใหม่โดยอัตโนมัติสำหรับผลิตภัณฑ์</span><span class="sxs-lookup"><span data-stu-id="4ac16-106">You can specify that you want to automatically reuse an existing configuration for a product.</span></span> <span data-ttu-id="4ac16-107">จากนั้น เมื่อผู้ใช้ดำเนินการรอบเวลาการตั้งค่าคอนฟิกเสร็จสมบูรณ์แล้ว ระบบจะตรวจสอบว่ามีการตั้งค่าคอนฟิกที่สอดคล้องกับการเลือกของผู้ใช้อยู่แล้วหรือไม่</span><span class="sxs-lookup"><span data-stu-id="4ac16-107">Then, when a user has completed a configuration session, the system verifies whether a configuration that matches the user’s selections already exists.</span></span> <span data-ttu-id="4ac16-108">ถ้าพบการตั้งค่าคอนฟิกที่ตรงกัน รหัสการตั้งค่าคอนฟิก ใบตราส่ง (BOM) ที่สอดคล้องกัน และกระบวนการผลิตจะถูกนำกลับมาใช้ใหม่</span><span class="sxs-lookup"><span data-stu-id="4ac16-108">If a matching configuration is found, the configuration ID, corresponding bill of materials (BOM), and route are reused.</span></span>

<a name="requirements-for-reusing-configurations"></a><span data-ttu-id="4ac16-109">ความต้องการสำหรับการตั้งค่าคอนฟิกที่นำมาใช้ใหม่</span><span class="sxs-lookup"><span data-stu-id="4ac16-109">Requirements for reusing configurations</span></span>
---------------------------------------

<span data-ttu-id="4ac16-110">เมื่อต้องการเปิดใช้งานให้นำการตั้งค่าคอนฟิกกลับมาใช้ใหม่ คุณต้องระบุข้อมูลต่อไปนี้สำหรับส่วนประกอบและแอททริบิวต์บนหน้า **รายละเอียดแบบจำลองการจัดโครงแบบผลิตภัณฑ์**:</span><span class="sxs-lookup"><span data-stu-id="4ac16-110">To enable configurations to be reused, you must specify the following information for the components and attributes on the **Product configuration model details** page:</span></span>

-   <span data-ttu-id="4ac16-111">**ส่วนประกอบและส่วนประกอบย่อย** บนแท็บด่วน **ทั่วไป** ในฟิลด์ **นำการตั้งค่าคอนฟิกมาใช้ใหม่** เลือก **ใช่**</span><span class="sxs-lookup"><span data-stu-id="4ac16-111">**Components and subcomponents** – On the **General** FastTab, in the **Reuse configurations** field, select **Yes**.</span></span>
-   <span data-ttu-id="4ac16-112">**แอททริบิวต์** – บนแท็บด่วน **แอททริบิวต์** เลือกตัวเลือก **รวมไว้ในการนำมาใช้ใหม่**</span><span class="sxs-lookup"><span data-stu-id="4ac16-112">**Attributes** – On the **Attributes** FastTab, select the **Include in reuse** option.</span></span> <span data-ttu-id="4ac16-113">ตัวเลือกนี้ปรากฏเฉพาะเมื่อส่วนประกอบที่เกี่ยวข้องถูกเปิดใช้งานสำหรับการนำมาใช้ใหม่</span><span class="sxs-lookup"><span data-stu-id="4ac16-113">This option appears only when the related component is enabled for reuse.</span></span> <span data-ttu-id="4ac16-114">ถ้าคุณไม่เลือกแอททริบิวต์ใดๆ สำหรับการนำมาใช้ใหม่ การตั้งค่าคอนฟิกจะถูกนำกลับมาใช้ใหม่เสมอ โดยไม่คำนึงถึงการเลือกของผู้ใช้ในระหว่างรอบเวลาการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="4ac16-114">If you don't select any attributes for reuse, the configuration is always reused, regardless of the user’s selections during a configuration session.</span></span> <span data-ttu-id="4ac16-115">ค่าแอททริบิวต์ในการตั้งค่าคอนฟิกที่มีอยู่ต้องตรงกับการเลือกของผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="4ac16-115">The attribute values in the existing configuration must match the user’s selections.</span></span> <span data-ttu-id="4ac16-116">ตัวอย่างเช่น ถ้าผู้ใช้เลือก **สีน้ำเงิน** เป็นสีในระหว่างรอบเวลาการตั้งค่าคอนฟิก ระบบจะตรวจสอบว่าการตั้งค่าคอนฟิกที่มีอยู่ของส่วนประกอบนั้นมีสีน้ำเงินหรือไม่</span><span class="sxs-lookup"><span data-stu-id="4ac16-116">For example, if the user selects **Blue** as the color during a configuration session, the system verifies whether an existing configuration of the component has the color blue.</span></span>

## <a name="resetting-configuration-reuse"></a><span data-ttu-id="4ac16-117">การรีเซ็ตการนำการตั้งค่าคอนฟิกมาใช้ใหม่</span><span class="sxs-lookup"><span data-stu-id="4ac16-117">Resetting configuration reuse</span></span>
<span data-ttu-id="4ac16-118">เมื่อคุณรีเซ็ตการนำการตั้งค่าคอนฟิกมาใช้ใหม่ จะไม่พิจารณาการตั้งค่าคอนฟิกที่สร้างขึ้นก่อนหน้านี้อีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="4ac16-118">When you reset configuration reuse, previously created configurations are no longer considered.</span></span> <span data-ttu-id="4ac16-119">คุณอาจต้องการรีเซ็ตการนำการตั้งค่าคอนฟิกมาใช้ใหม่ถ้า BOM หรือกระบวนการผลิตมีการเปลี่ยนแปลง แต่ไม่มีการเปลี่ยนแปลงแอททริบิวต์ที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="4ac16-119">You might want to reset configuration reuse if the BOM or route was changed, but no related attributes were changed.</span></span> <span data-ttu-id="4ac16-120">คุณรีเซ็ตการนำการตั้งค่าคอนฟิกมาใช้ใหม่ในแท็บด่วน **ทั่วไป** สำหรับส่วนประกอบ</span><span class="sxs-lookup"><span data-stu-id="4ac16-120">You reset configuration reuse on the **General** FastTab for the component.</span></span>




