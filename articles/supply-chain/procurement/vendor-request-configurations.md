---
title: การตั้งค่าคอนฟิกคำขอของผู้จัดจำหน่าย
description: หัวข้อนี้อธิบายถึงฟิลด์ที่จำเป็นต้องถูกเติมข้อมูลในคำขอของผู้จัดจำหน่ายใหม่
author: mkirknel
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationConfig
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: d78aa7c14ed2a2a5097f6f80c946c6ae4ed8bb94
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208097"
---
# <a name="vendor-request-configurations"></a><span data-ttu-id="db833-103">การตั้งค่าคอนฟิกคำขอของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="db833-103">Vendor request configurations</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="db833-104">เมื่อต้องการดำเนินการคำขอของผู้จัดจำหน่ายให้เสร็จสมบูรณ์ ผู้ติดต่อของผู้จัดจำหน่ายต้องดำเนินการตัวช่วยสร้างการลงทะเบียนผู้ที่มีแนวโน้มจะเป็นผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="db833-104">To complete a vendor request, a vendor contact person must complete the prospective vendor registration wizard.</span></span>

<span data-ttu-id="db833-105">ในแบบฟอร์ม **การตั้งค่าคอนฟิกคำขอของผู้จัดจำหน่าย** คุณสามารถสร้างโพรไฟล์ที่ระบุฟิลด์ที่จำเป็นและฟิลด์ที่มองเห็นได้ในตัวช่วยสร้างการลงทะเบียนผู้ที่มีแนวโน้มจะเป็นผู้จัดจำหน่ายได้</span><span class="sxs-lookup"><span data-stu-id="db833-105">In the **Vendor request configurations** form, you can create profiles that specify required fields and visible fields in the prospective vendor registration wizard.</span></span>

<span data-ttu-id="db833-106">ตัวช่วยสร้างการลงทะเบียนผู้จัดจำหน่ายจะเริ่มโดยการร้องขอผู้ใช้ของผู้ที่มีแนวโน้มจะเป็นผู้จัดจำหน่ายที่ซึ่งประเทศ/ภูมิภาคที่ผู้จัดจำหน่ายทำธุรกิจอยู่</span><span class="sxs-lookup"><span data-stu-id="db833-106">The vendor registration wizard will start out by asking the prospective vendor user which country/region the vendor is doing business in.</span></span> <span data-ttu-id="db833-107">ข้อมูลนี้กำหนดโครงแบบที่เกี่ยวข้อง</span><span class="sxs-lookup"><span data-stu-id="db833-107">This information determines the applicable configuration.</span></span> <span data-ttu-id="db833-108">ถ้าไม่มีการตั้งค่าคอนฟิกเฉพาะไว้สำหรับประเทศ/ภูมิภาค จะมีการใช้การตั้งค่าคอนฟิกเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="db833-108">If no specific configuration is defined for a country/region, a default configuration will be used.</span></span>

### <a name="set-up-a-vendor-request-configuration"></a><span data-ttu-id="db833-109">ตั้งค่าการตั้งค่าคอนฟิกคำขอของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="db833-109">Set up a vendor request configuration</span></span>

<span data-ttu-id="db833-110">โดยค่าเริ่มต้น มีการตั้งค่าคอนฟิกผู้จัดจำหน่ายอยู่ในแบบฟอร์มการตั้งค่าคอนฟิกคำขอของผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="db833-110">By default, there is a vendor configuration available in the Vendor request configurations form.</span></span>

<span data-ttu-id="db833-111">ไม่สามารถเลือกประเทศ/ภูมิภาคสำหรับการตั้งค่าคอนฟิกเริ่มต้นได้ ดังนั้นส่วน **ประเทศ/ภูมิภาค** จึงไม่สามารถเปลี่ยนแปลงได้</span><span class="sxs-lookup"><span data-stu-id="db833-111">It is not possible to select country/regions for the default configuration, so the **Countries/regions** section cannot be changed.</span></span>

1. <span data-ttu-id="db833-112">คลิก **การจัดซื้อและการจัดหา** > **การตั้งค่า** > **ผู้จัดจำหน่าย** แล้วจากนั้นคลิก **การตั้งค่าคอนฟิกคำขอของผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="db833-112">Click **Procurement and sourcing** > **Setup** > **Vendors**, and then click **Vendor request configurations**.</span></span>
2. <span data-ttu-id="db833-113">คลิกแท็บ **ฟิลด์** เพื่อตั้งค่าสถานะของฟิลด์ที่แสดงรายการ</span><span class="sxs-lookup"><span data-stu-id="db833-113">Click the **Fields** tab to set the status of the listed fields.</span></span>
3. <span data-ttu-id="db833-114">ซ่อน (ไม่สามารถมองเห็นได้)</span><span class="sxs-lookup"><span data-stu-id="db833-114">Hidden (Not visible)</span></span>
4. <span data-ttu-id="db833-115">แสดง (มองเห็นได้ แต่ไม่ใช่ข้อมูลบังคับ)</span><span class="sxs-lookup"><span data-stu-id="db833-115">Displayed (Visible but not mandatory)</span></span>
5. <span data-ttu-id="db833-116">จำเป็น (มองเห็นได้ และบังคับ)</span><span class="sxs-lookup"><span data-stu-id="db833-116">Required (Visible and mandatory)</span></span>
6. <span data-ttu-id="db833-117">คลิกแท็บ **เนื้อหา** เพื่อระบุว่าข้อความที่จะแสดงในวิซาร์ดหรือไม่ และควรมีการยอมรับว่าผู้ที่มีแนวโน้มจะเป็นผู้จัดจำหน่ายต้องยอมรับรายการนี้ ก่อนที่จะย้ายไปยังขั้นตอนถัดไปในวิซาร์ดหรือไม่</span><span class="sxs-lookup"><span data-stu-id="db833-117">Click the **Content** tab to specify if text is going to be shown on the wizard and if there should be an acknowledgement that the prospective vendor user must accept this before moving to the next step in the wizard.</span></span> <span data-ttu-id="db833-118">การยอมรับจะถูกร้องขอสำหรับข้อกำหนดและเงื่อนไขใดๆ ที่ผู้ใช้ต้องยอมรับเพื่อดำเนินต่อ</span><span class="sxs-lookup"><span data-stu-id="db833-118">The acknowledgement will be requested for any terms and conditions that the user must accept to continue.</span></span>

<span data-ttu-id="db833-119">คุณยังสามารถป้อนข้อความยืนยันที่จะแสดงเมื่อเสร็จสิ้นวิซาร์ด และคุณสามารถเพิ่มแบบสอบถามได้หนึ่งรายการขึ้นไป</span><span class="sxs-lookup"><span data-stu-id="db833-119">You can also enter a confirmation message that will be displayed when the wizard is finalized, and you can add one or more questionnaires.</span></span>

### <a name="create-a-vendor-configuration-for-a-specific-countryregion"></a><span data-ttu-id="db833-120">สร้างการตั้งค่าคอนฟิกผู้จัดจำหน่ายสำหรับประเทศ/ภูมิภาคที่เฉพาะเจาะจง</span><span class="sxs-lookup"><span data-stu-id="db833-120">Create a vendor configuration for a specific country/region</span></span>
1.  <span data-ttu-id="db833-121">คลิก **การจัดซื้อและการจัดหา** > **การตั้งค่า** > **ผู้จัดจำหน่าย** แล้วจากนั้นคลิก **การตั้งค่าคอนฟิกคำขอของผู้จัดจำหน่าย**</span><span class="sxs-lookup"><span data-stu-id="db833-121">Click **Procurement and sourcing** > **Setup** > **Vendors**, and then click **Vendor request configurations**.</span></span>
2.  <span data-ttu-id="db833-122">คลิก **สร้าง** เพื่อสร้างโครงแบบใหม่ และระบุชื่อสำหรับการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="db833-122">Click **New** to create a new configuration, and provide a name for the configuration.</span></span>
3.  <span data-ttu-id="db833-123">คลิก **บันทึก**</span><span class="sxs-lookup"><span data-stu-id="db833-123">Click **Save**.</span></span>
4.  <span data-ttu-id="db833-124">เปิดแท็บ **ประเทศ/ภูมิภาค** เพื่อเลือกประเทศ/ภูมิภาคที่ควรใช้สำหรับการตั้งค่าคอนฟิก</span><span class="sxs-lookup"><span data-stu-id="db833-124">Open the **Country/regions** tab to select the country/region that the configuration should be used for.</span></span>
5.  <span data-ttu-id="db833-125">ตั้งค่าคอนฟิกให้เสร็จสมบูรณ์ โดยทำตามคำแนะนำสำหรับการตั้งค่าคอนฟิกเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="db833-125">Complete the configuration by following the guidelines for the default configuration.</span></span>

