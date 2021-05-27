---
title: คุณไม่สามารถใช้เท็มเพลตกับผลิตภัณฑ์ที่นำออกใช้ได้
description: คุณไม่สามารถใช้เท็มเพลตกับผลิตภัณฑ์ที่นำออกใช้ได้
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1ad6efdced9bce924fbf5bc207c92fa2c3a6c79d
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026942"
---
# <a name="you-cant-apply-a-template-to-create-a-released-product"></a><span data-ttu-id="7cf54-103">คุณไม่สามารถใช้เท็มเพลตเพื่อสร้างผลิตภัณฑ์ที่นำออกใช้ได้</span><span class="sxs-lookup"><span data-stu-id="7cf54-103">You can't apply a template to create a released product</span></span>

<span data-ttu-id="7cf54-104">หมายเลข KB: 4612097</span><span class="sxs-lookup"><span data-stu-id="7cf54-104">KB number: 4612097</span></span>

## <a name="symptoms"></a><span data-ttu-id="7cf54-105">อาการ</span><span class="sxs-lookup"><span data-stu-id="7cf54-105">Symptoms</span></span>

<span data-ttu-id="7cf54-106">เมื่อคุณสร้างผลิตภัณฑ์ที่นำออกใช้ใหม่โดยใช้กล่องโต้ตอบ **ผลิตภัณฑ์ที่นำออกใช้ใหม่** คุณสามารถเลือกเท็มเพลตได้</span><span class="sxs-lookup"><span data-stu-id="7cf54-106">When you create a new released product by using the **New released product** dialog box, you can select a template.</span></span> <span data-ttu-id="7cf54-107">เท็มเพลตควรระบุการตั้งค่าเริ่มต้นสำหรับฟิลด์หลายฟิลด์ของผลิตภัณฑ์ที่นำออกใช้ใหม่</span><span class="sxs-lookup"><span data-stu-id="7cf54-107">The template is supposed to provide default settings for many fields of the new released product.</span></span> <span data-ttu-id="7cf54-108">อย่างไรก็ตาม ฟิลด์บางฟิลด์หรือทั้งหมดไม่ได้รับการตั้งค่า หลังจากที่คุณเลือกเท็มเพลต</span><span class="sxs-lookup"><span data-stu-id="7cf54-108">However, some or all of the fields aren't set after you select the template.</span></span>

## <a name="cause"></a><span data-ttu-id="7cf54-109">สาเหตุ</span><span class="sxs-lookup"><span data-stu-id="7cf54-109">Cause</span></span>

<span data-ttu-id="7cf54-110">หน้าหลายหน้าใน Microsoft Dynamics 365 Supply Chain Management ช่วยให้คุณสามารถสร้างเท็มเพลตที่สร้างการตั้งค่าเริ่มต้นสำหรับเรกคอร์ดที่แสดงบนหน้าเหล่านั้น</span><span class="sxs-lookup"><span data-stu-id="7cf54-110">Many pages in Microsoft Dynamics 365 Supply Chain Management let you create a template that establishes initial settings for the records that are shown on those pages.</span></span> <span data-ttu-id="7cf54-111">คุณสามารถสร้างเท็มเพลตใดเท็มเพลตหนึ่งเหล่านี้โดยการเลือก **ข้อมูลเรกคอร์ด** บนแท็บ **ตัวเลือก** ของบานหน้าต่างการดำเนินการ</span><span class="sxs-lookup"><span data-stu-id="7cf54-111">You can create one of these templates by selecting **Record info** on the **Options** tab of the Action Pane.</span></span> <span data-ttu-id="7cf54-112">อย่างไรก็ตาม ผลิตภัณฑ์ที่นำออกใช้จะซับซ้อนกว่าเรกคอร์ดชนิดอื่นๆ อย่างมาก</span><span class="sxs-lookup"><span data-stu-id="7cf54-112">However, released products are much more complex than most other types of records.</span></span> <span data-ttu-id="7cf54-113">ถึงแม้ว่าคุณจะสามารถเลือก **ข้อมูลเรกคอร์ด** ในหน้า **ผลิตภัณฑ์ที่นำออกใช้** เพื่อสร้างเท็มเพลตได้ และแม้ว่าคุณจะสามารถเลือกเท็มเพลตนั้น เมื่อคุณสร้างผลิตภัณฑ์ที่นำออกใช้ แต่เท็มเพลตจะไม่ระบุค่าฟิลด์ที่คาดไว้สำหรับผลิตภัณฑ์ที่นำออกใช้ใหม่</span><span class="sxs-lookup"><span data-stu-id="7cf54-113">Although you can select **Record info** on the **Released products** page to create a template, and although you can select that template when you create a released product, the template won't provide the expected field values for the new released product.</span></span> <span data-ttu-id="7cf54-114">ดังนั้น คุณจึงไม่สามารถใช้เท็มเพลต "ข้อมูลเรกคอร์ด" สำหรับผลิตภัณฑ์ที่นำออกใช้ได้</span><span class="sxs-lookup"><span data-stu-id="7cf54-114">Therefore, you can't use "record info" templates for released products.</span></span> <span data-ttu-id="7cf54-115">แต่คุณต้องสร้างเท็มเพลตผลิตภัณฑ์เฉพาะ</span><span class="sxs-lookup"><span data-stu-id="7cf54-115">Instead, you must create dedicated product templates.</span></span>

## <a name="resolution"></a><span data-ttu-id="7cf54-116">ความละเอียด</span><span class="sxs-lookup"><span data-stu-id="7cf54-116">Resolution</span></span>

<span data-ttu-id="7cf54-117">เมื่อต้องการสร้างเท็มเพลตผลิตภัณฑ์ ให้ใช้เมนู **เท็มเพลต** บนแท็บ **ผลิตภัณฑ์** ของบานหน้าต่างการดำเนินการ ไม่ใช่ปุ่ม **ข้อมูลเรกคอร์ด** บนแท็บ **ตัวเลือก**</span><span class="sxs-lookup"><span data-stu-id="7cf54-117">To create a product template, use the **Template** menu on the **Product** tab of the Action Pane, not the **Record info** button on the **Options** tab.</span></span>

1. <span data-ttu-id="7cf54-118">ไปยัง **การจัดการข้อมูลผลิตภัณฑ์ \> ผลิตภัณฑ์ \> ผลิตภัณฑ์ที่นำออกใช้**</span><span class="sxs-lookup"><span data-stu-id="7cf54-118">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="7cf54-119">บนบานหน้าต่างการดำเนินการ บนแท็บ **ผลิตภัณฑ์** ในกลุ่ม **ใหม่** เลือก **เท็มเพลต** แล้วจากนั้น เลือก **สร้างเท็มเพลตส่วนบุคคล** หรือ **สร้างเท็มเพลตที่ใช้ร่วมกัน** ตามความเหมาะสม</span><span class="sxs-lookup"><span data-stu-id="7cf54-119">On the Action Pane, on the **Product** tab, in the **New** group, select **Template**, and then select either **Create personal template** or **Create shared template**, as appropriate.</span></span>
