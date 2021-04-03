---
title: ประวัติเหตุการณ์ของสินทรัพย์
description: หัวข้อนี้อธิบายวิธีการเข้าถึงประวัติเหตุการณ์ของสินทรัพย์ในการจัดการสินทรัพย์
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1bcec99b811c67eca5473242820d8539758a5872
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253145"
---
# <a name="asset-event-history"></a><span data-ttu-id="b49cb-103">ประวัติเหตุการณ์ของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="b49cb-103">Asset event history</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="b49cb-104">หัวข้อนี้อธิบายวิธีการเข้าถึงประวัติเหตุการณ์ของสินทรัพย์ในการจัดการสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="b49cb-104">This topic explains how to access asset event history in Asset Management.</span></span> <span data-ttu-id="b49cb-105">หน้า **ประวัติเหตุการณ์ของสินทรัพย์** แสดงประวัติการลงทะเบียนที่ได้มีการสร้างในช่วงอายุการใช้งานของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="b49cb-105">The **Asset event history** page shows the registration history that has been made during the lifetime of an asset.</span></span> <span data-ttu-id="b49cb-106">คุณสามารถเข้าถึงหน้านี้จากรายการเมนู **สินทรัพย์ทั้งหมด** **สินทรัพย์ที่ใช้งานอยู่** และ **สินทรัพย์ที่ใช้งานอยู่ของฉัน**</span><span class="sxs-lookup"><span data-stu-id="b49cb-106">You can access this page from the **All assets**, **Active assets**, and **My active assets** menu items.</span></span> <span data-ttu-id="b49cb-107">เลือกสินทรัพย์ และจากนั้น เลือก **ประวัติเหตุการณ์**</span><span class="sxs-lookup"><span data-stu-id="b49cb-107">Select an asset, and then select **Event history**.</span></span>

<span data-ttu-id="b49cb-108">บน FastTab **รายละเอียด** ของหน้า **ประวัติเหตุการณ์ของสินทรัพย์** คุณสามารถค้นหาได้ในข้อมูลที่มีอยู่ทั้งหมด</span><span class="sxs-lookup"><span data-stu-id="b49cb-108">On the **Details** FastTab of the **Asset event history** page, you can do a search on all the available information.</span></span> <span data-ttu-id="b49cb-109">ตัวอย่างเช่น คุณสามารถใช้ประวัติเหตุการณ์ของสินทรัพย์เพื่อค้นหาข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b49cb-109">For example, you can use the asset event history to find the following information:</span></span>

- <span data-ttu-id="b49cb-110">เวลาที่มีการใช้ชนิดงานล่าสุดในสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="b49cb-110">When a job type was last used on an asset</span></span>
- <span data-ttu-id="b49cb-111">เมื่อผู้ปฏิบัติงานเฉพาะป้อนหมายเหตุในงานของใบสั่งงาน</span><span class="sxs-lookup"><span data-stu-id="b49cb-111">When a specific worker entered a remark on a work order job</span></span>

<span data-ttu-id="b49cb-112">เส้นเวลาจะถูกปรับปรุงทุกครั้งที่มีการเปิดหน้านั้น</span><span class="sxs-lookup"><span data-stu-id="b49cb-112">The timeline is updated every time that the page is opened.</span></span> <span data-ttu-id="b49cb-113">ซึ่งประกอบด้วยข้อมูลต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="b49cb-113">It contains the following information:</span></span>

- <span data-ttu-id="b49cb-114">การเปลี่ยนแปลงที่ได้ถูกสร้างขึ้นในสินทรัพย์: สถานที่ของสินทรัพย์ รหัสสินทรัพย์ ชื่อ และการรับประกันผู้จัดจำหน่าย</span><span class="sxs-lookup"><span data-stu-id="b49cb-114">Changes that have been made on the asset: asset location, asset ID, name, and vendor warranty</span></span>
- <span data-ttu-id="b49cb-115">รายการหลักของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="b49cb-115">Asset parent</span></span>
- <span data-ttu-id="b49cb-116">สูตรการผลิตของสินทรัพย์ (BOM)</span><span class="sxs-lookup"><span data-stu-id="b49cb-116">Asset bill of materials (BOM)</span></span>
- <span data-ttu-id="b49cb-117">ล็อกสถานะของวงจรการใช้ของสินทรัพย์</span><span class="sxs-lookup"><span data-stu-id="b49cb-117">Asset lifecycle state log</span></span>
- <span data-ttu-id="b49cb-118">ตำแหน่งที่ทำงาน</span><span class="sxs-lookup"><span data-stu-id="b49cb-118">Functional location</span></span>
- <span data-ttu-id="b49cb-119">คำขอการบำรุงรักษา</span><span class="sxs-lookup"><span data-stu-id="b49cb-119">Maintenance requests</span></span>
- <span data-ttu-id="b49cb-120">ใบสั่งงาน ซึ่งรวมถึงสินค้าและบันทึกย่อที่ลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="b49cb-120">Work orders, including posted item and notes</span></span>
- <span data-ttu-id="b49cb-121">ข้อบกพร่อง</span><span class="sxs-lookup"><span data-stu-id="b49cb-121">Faults</span></span>
- <span data-ttu-id="b49cb-122">การประเมินเงื่อนไข</span><span class="sxs-lookup"><span data-stu-id="b49cb-122">Condition assessments</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]