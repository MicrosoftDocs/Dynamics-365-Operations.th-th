---
title: เครื่องมือแก้ไขสูตรการรายงานทางอิเล็กทรอนิกส์ขั้นสูง
description: หัวข้อนี้อธิบายวิธีการใช้ตัวแก้ไขสูตรขั้นสูงเพื่อกำหนดค่านิพจน์ในการแม็ปโมเดลการรายงานทางอิเล็กทรอนิกส์ (ER) กับส่วนประกอบรูปแบบ
author: NickSelin
ms.date: 06/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: f7f80928e1d3f5d4892f72d4bd2fd09b70a26c1f
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270718"
---
# <a name="electronic-reporting-advanced-formula-editor"></a><span data-ttu-id="a6e3d-103">เครื่องมือแก้ไขสูตรการรายงานทางอิเล็กทรอนิกส์ขั้นสูง</span><span class="sxs-lookup"><span data-stu-id="a6e3d-103">Electronic reporting advanced formula editor</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a6e3d-104">นอกจากนี้ [การรายงานทางอิเล็กทรอนิกส์](general-electronic-reporting.md) [ตัวแก้ไขสูตร](general-electronic-reporting-formula-designer.md) คุณสามารถใช้ตัวแก้ไขสูตรการรายงานทางอิเล็กทรอนิกส์ขั้นสูงเพื่อปรับปรุงประสบการณ์ของการกำหนดค่านิพจน์การรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="a6e3d-104">In addition to the [Electronic reporting](general-electronic-reporting.md) [formula editor](general-electronic-reporting-formula-designer.md), you can use the advanced Electronic reporting formula editor to improve the experience of configuring Electronic reporting (ER) expressions.</span></span> <span data-ttu-id="a6e3d-105">ตัวแก้ไขขั้นสูงใช้เบราว์เซอร์และดำเนินการโดย [ตัวแก้ไข Monaco](https://microsoft.github.io/monaco-editor)</span><span class="sxs-lookup"><span data-stu-id="a6e3d-105">The advanced editor is browser-based and powered by the [Monaco editor](https://microsoft.github.io/monaco-editor).</span></span> <span data-ttu-id="a6e3d-106">คุณลักษณะตัวแก้ไขขั้นสูงที่ใช้บ่อยที่สุดมีการอธิบายไว้ในหัวข้อนี้:</span><span class="sxs-lookup"><span data-stu-id="a6e3d-106">The most commonly used advanced editor features are described in this topic:</span></span>

- [<span data-ttu-id="a6e3d-107">การจัดรูปแบบอัตโนมัติของรหัส</span><span class="sxs-lookup"><span data-stu-id="a6e3d-107">Code autoformatting</span></span>](#Autoformatting)
- [<span data-ttu-id="a6e3d-108">IntelliSense</span><span class="sxs-lookup"><span data-stu-id="a6e3d-108">IntelliSense</span></span>](#IntelliSense)
- [<span data-ttu-id="a6e3d-109">การทำรหัสให้เสร็จสมบูรณ์</span><span class="sxs-lookup"><span data-stu-id="a6e3d-109">Code completion</span></span>](#CodeCompletion)
- [<span data-ttu-id="a6e3d-110">การนำทางรหัส</span><span class="sxs-lookup"><span data-stu-id="a6e3d-110">Code navigation</span></span>](#CodeNavigation)
- [<span data-ttu-id="a6e3d-111">กำหนดโครงสร้างรหัส</span><span class="sxs-lookup"><span data-stu-id="a6e3d-111">Code structuring</span></span>](#CodeStructuring)
- [<span data-ttu-id="a6e3d-112">ค้นหาและแทนที่</span><span class="sxs-lookup"><span data-stu-id="a6e3d-112">Find and replace</span></span>](#FindAndReplace)
- [<span data-ttu-id="a6e3d-113">การวางข้อมูล</span><span class="sxs-lookup"><span data-stu-id="a6e3d-113">Data pasting</span></span>](#DataPasting)
- [<span data-ttu-id="a6e3d-114">การทำสีที่ไวยากรณ์</span><span class="sxs-lookup"><span data-stu-id="a6e3d-114">Syntax colorization</span></span>](#SyntaxColorization)

## <a name=""></a><span data-ttu-id="a6e3d-115"><a name="ActivateAdvEditor">เริ่มการใช้งานตัวแก้ไขสูตรขั้นสูง</a></span><span class="sxs-lookup"><span data-stu-id="a6e3d-115"><a name="ActivateAdvEditor">Activate the advanced formula editor</a></span></span>

<span data-ttu-id="a6e3d-116">ทำตามขั้นตอนต่อไปนี้เพื่อเริ่มใช้ตัวแก้ไขสูตรขั้นสูงในอินสแตนซ์ Microsoft Dynamics 365 Finance ของคุณ</span><span class="sxs-lookup"><span data-stu-id="a6e3d-116">Complete the following steps to start using the advanced formula editor in your instance of Microsoft Dynamics 365 Finance.</span></span>

1.  <span data-ttu-id="a6e3d-117">ไปที่ **การจัดการองค์กร** \> **การรายงานทางอิเล็กทรอนิกส์** \> **การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="a6e3d-117">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2.  <span data-ttu-id="a6e3d-118">ในหน้า **การตั้งค่าคอนฟิก** บนบานหน้าต่างการดำเนินการ บนแท็บ **การตั้งค่าคอนฟิก** ในกลุ่ม **การตั้งค่าล่วงหน้า** เลือก **พารามิเตอร์ผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="a6e3d-118">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3.  <span data-ttu-id="a6e3d-119">กล่องโต้ตอบ **พารามิเตอร์ผู้ใช้** ในส่วน **การติดตามการดำเนินการ** ตั้งค่าพารามิเตอร์ **ตัวแก้ไขสูตรขั้นสูง** เป็น **ใช่**</span><span class="sxs-lookup"><span data-stu-id="a6e3d-119">In the **User parameters** dialog box, in the **Execution tracing** section, set the **Enable advanced formula editor** parameter to **Yes**.</span></span>

<span data-ttu-id="a6e3d-120">[![กล่องโต้ตอบพารามิเตอร์ผู้ใช้ เปิดใช้งานพารามิเตอร์โปรแกรมแก้ไขสูตรขั้นสูงที่เน้น](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)</span><span class="sxs-lookup"><span data-stu-id="a6e3d-120">[![User parameters dialog box, Enable advanced formula editor parameter highlighted](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)</span></span>

> [!NOTE]
> <span data-ttu-id="a6e3d-121">พึงระวังว่าพารามิเตอร์นี้เฉพาะผู้ใช้และเฉพาะบริษัท</span><span class="sxs-lookup"><span data-stu-id="a6e3d-121">Be aware that this parameter is user specific and company specific.</span></span>

<span data-ttu-id="a6e3d-122">เริ่มต้นใน Microsoft Dynamics 365 Finance รุ่น 10.0.19 คุณสามารถควบคุมตัวแก้ไขสูตร ER ที่เสนอไว้ตามค่าเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="a6e3d-122">Starting in Microsoft Dynamics 365 Finance version 10.0.19, you can control what ER formula editor is offered by default.</span></span> <span data-ttu-id="a6e3d-123">ปฏิบัติตามขั้นตอนต่อไปนี้เพื่อเปิดใช้งานตัวแก้ไขสูตรขั้นสูงของผู้ใช้และบริษัททั้งหมดของอินสแตนซ์การเงินปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="a6e3d-123">Complete the following steps to enable the advanced formula editor for all users and companies of the current Finance instance.</span></span>

1.  <span data-ttu-id="a6e3d-124">เปิดพื้นที่ทำงาน **การจัดการคุณลักษณะ**</span><span class="sxs-lookup"><span data-stu-id="a6e3d-124">Open the **Feature management** workspace.</span></span>
2.  <span data-ttu-id="a6e3d-125">ค้นหาและเลือกคุณลักษณะ **ตั้งค่าเครื่องมือแก้ไขขั้นสูง ER เป็นเครื่องมือเริ่มต้นของผู้ใช้ทั้งหมด** ในรายการ แล้วเลือก **เปิดใช้งานทันที**</span><span class="sxs-lookup"><span data-stu-id="a6e3d-125">Find and select the feature **Set the ER advanced formula editor as the default one for all users** in the list, and then select **Enable now**.</span></span>
3.  <span data-ttu-id="a6e3d-126">ไปที่ **การจัดการองค์กร** > **การรายงานทางอิเล็กทรอนิกส์** > **การตั้งค่าคอนฟิก**</span><span class="sxs-lookup"><span data-stu-id="a6e3d-126">Go to **Organization administration** > **Electronic reporting** > **Configurations**.</span></span>
4.  <span data-ttu-id="a6e3d-127">ในหน้า **การตั้งค่าคอนฟิก** บนบานหน้าต่างการดำเนินการ บนแท็บ **การตั้งค่าคอนฟิก** ในกลุ่ม **การตั้งค่าล่วงหน้า** เลือก **พารามิเตอร์ผู้ใช้**</span><span class="sxs-lookup"><span data-stu-id="a6e3d-127">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
5.  <span data-ttu-id="a6e3d-128">ในกล่องโต้ตอบ **พารามิเตอร์ผู้ใช้** ให้ค้นหาพารามิเตอร์ **ปิดใช้งานเครื่องมือแก้ไขสูตรขั้นสูง** และตรวจสอบว่ามีการตั้งค่าเป็น **ไม่**</span><span class="sxs-lookup"><span data-stu-id="a6e3d-128">In the **User parameters** dialog box, find the **Disable advanced formula editor** parameter and verify that it is set to **No**.</span></span>

<span data-ttu-id="a6e3d-129">[![กล่องโต้ตอบพารามิเตอร์ผู้ใช้ ปิดใช้งานพารามิเตอร์โปรแกรมแก้ไขสูตรขั้นสูงที่เน้น](./media/ER-AdvEditor-Activate2.png)](./media/ER-AdvEditor-Activate2.png)</span><span class="sxs-lookup"><span data-stu-id="a6e3d-129">[![User parameters dialog box, Disable advanced formula editor parameter highlighted](./media/ER-AdvEditor-Activate2.png)](./media/ER-AdvEditor-Activate2.png)</span></span>

> [!NOTE]
> <span data-ttu-id="a6e3d-130">ค่าของพารามิเตอร์ **เปิดใช้งานเครื่องมือแก้ไขสูตรขั้นสูง** และ **ปิดใช้งานเครื่องมือแก้ไขสูตรขั้นสูง** จะถูกแยกไว้โดยผู้ใช้แต่ละคน และเสนอในกล่องโต้ตอบ **พารามิเตอร์ผู้ใช้** ทั้งนี้ขึ้นอยู่กับสถานะของคุณลักษณะ **ตั้งค่าเครื่องมือแก้ไขขั้นสูง ER เป็นเครื่องมือเริ่มต้นของผู้ใช้ทั้งหมด**</span><span class="sxs-lookup"><span data-stu-id="a6e3d-130">The values of the parameters **Enable advanced formula editor** and **Disable advanced formula editor** are kept separate for each user and offered on the **User parameters** dialog box depending on the status of the **Set the ER advanced formula editor as the default one for all users** feature.</span></span>

## <a name=""></a><span data-ttu-id="a6e3d-131"><a name="Autoformatting">การจัดรูปแบบอัตโนมัติของรหัส</a></span><span class="sxs-lookup"><span data-stu-id="a6e3d-131"><a name="Autoformatting">Code autoformatting</a></span></span>

<span data-ttu-id="a6e3d-132">เมื่อคุณเขียนนิพจน์ที่ซับซ้อนที่ประกอบด้วยรหัสหลายแถว การเยื้องของบรรทัดที่ป้อนใหม่จะเป็นไปโดยอัตโนมัติตามการเยื้องของแถวก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="a6e3d-132">When you write a complex expression that consists of multiple rows of code, the indentation of a new entered line will be automatic based on the indentation of the previous row.</span></span> <span data-ttu-id="a6e3d-133">คุณสามารถเลือกบรรทัดและเปลี่ยนการเยื้องได้โดยพิมพ์ **Tab** หรือ **Shift+Tab**.</span><span class="sxs-lookup"><span data-stu-id="a6e3d-133">You can select lines and change their indentation by typing **Tab** or **Shift+Tab**.</span></span>

<span data-ttu-id="a6e3d-134">[![GIF เครื่องมือแก้ไขสูตรขั้นสูง ER ที่แสดงรายการที่เลือกและการเปลี่ยนการเยื้อง](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)</span><span class="sxs-lookup"><span data-stu-id="a6e3d-134">[![ER formula editor gif showing selecting lines and changing the indentation](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)</span></span>

<span data-ttu-id="a6e3d-135">การจัดรูปแบบอัตโนมัติช่วยให้คุณสามารถรักษานิพจน์ทั้งหมดให้อยู่ในรูปแบบที่ดีเพื่อให้การบำรุงรักษาง่ายขึ้นและทำให้เข้าใจตรรกะที่กำหนดค่าได้ง่ายขึ้น</span><span class="sxs-lookup"><span data-stu-id="a6e3d-135">Autoformatting allows you to keep the entire expression well formatted to make further maintenance easier and to simplify understanding of the configured logic.</span></span>

## <a name=""></a><span data-ttu-id="a6e3d-136"><a name="IntelliSense">IntelliSense</a></span><span class="sxs-lookup"><span data-stu-id="a6e3d-136"><a name="IntelliSense">IntelliSense</a></span></span>

<span data-ttu-id="a6e3d-137">ตัวแก้ไขสนับสนุนการกรอกคำให้เสร็จสมบูรณ์เพื่อช่วยให้คุณเขียนนิพจน์ได้เร็วขึ้นและหลีกเลี่ยงการพิมพ์ผิด</span><span class="sxs-lookup"><span data-stu-id="a6e3d-137">The editor provides word completion to help you write expression faster and avoid typos.</span></span> <span data-ttu-id="a6e3d-138">เมื่อคุณเริ่มเพิ่มข้อความใหม่ ตัวแก้ไขนำเสนอรายการฟังก์ชันที่สนับสนุนในฟังก์ชัน ER โดยอัตโนมัติซึ่งมีอักขระที่คุณได้ป้อนไว้</span><span class="sxs-lookup"><span data-stu-id="a6e3d-138">When you start adding new text, the editor automatically offers a list of functions supported in ER functions that contain the characters you have entered.</span></span> <span data-ttu-id="a6e3d-139">คุณยังสามารถแสดงทริกเกอร์ IntelliSense ในสถานที่ใด ๆ ของนิพจน์ที่กำหนดค่าไว้โดยการพิมพ์ **Ctrl+Space**</span><span class="sxs-lookup"><span data-stu-id="a6e3d-139">You can also trigger IntelliSense in any place of a configured expression by typing **Ctrl+Space**.</span></span>

<span data-ttu-id="a6e3d-140">[![GIF เครื่องมือแก้ไขสูตรขั้นสูง ER ที่แสดงการทริกเกอร์ IntelliSense](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)</span><span class="sxs-lookup"><span data-stu-id="a6e3d-140">[![ER formula editor gif showing triggering IntelliSense](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)</span></span>

## <a name=""></a><span data-ttu-id="a6e3d-141"><a name="CodeCompletion">การทำรหัสให้เสร็จสมบูรณ์</a></span><span class="sxs-lookup"><span data-stu-id="a6e3d-141"><a name="CodeCompletion">Code completion</a></span></span>

<span data-ttu-id="a6e3d-142">ตัวแก้ไขจัดเตรียมการกรอกรหัสให้สมบูรณ์โดยอัตโนมัติโดย:</span><span class="sxs-lookup"><span data-stu-id="a6e3d-142">The editor automatically provides code completion by:</span></span>

- <span data-ttu-id="a6e3d-143">การแทรกวงเล็บปิดเมื่อป้อนวงเล็บเปิดไว้ และทำให้เคอร์เซอร์อยู่ในเครื่องหมายวงเล็บ</span><span class="sxs-lookup"><span data-stu-id="a6e3d-143">Inserting a closing bracket when an opening  bracket is entered, keeping the cursor inside the brackets.</span></span>
- <span data-ttu-id="a6e3d-144">การแทรกสัญลักษณ์คำพูดที่สองเมื่อป้อนตัวแรก และทำให้เคอร์เซอร์อยู่ในเครื่องหมายคำพูด</span><span class="sxs-lookup"><span data-stu-id="a6e3d-144">Inserting the second quotation symbol when the first one is entered, keeping the cursor inside the quotations.</span></span>
- <span data-ttu-id="a6e3d-145">การแทรกสัญลักษณ์คำพูดคู่ที่สองเมื่อป้อนตัวแรก และทำให้เคอร์เซอร์อยู่ในเครื่องหมายคำพูด</span><span class="sxs-lookup"><span data-stu-id="a6e3d-145">Inserting the second double quotation symbol when the first one is entered, keeping the cursor inside the quotations.</span></span>

<span data-ttu-id="a6e3d-146">[![GIF เครื่องมือแก้ไขสูตรขั้นสูง ER ที่แสดงเครื่องมือแก้ไขให้การเสร็จสมบูรณ์ของรหัสโดยอัตโนมัติ](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)</span><span class="sxs-lookup"><span data-stu-id="a6e3d-146">[![ER formula editor gif showing the editor automatically providing code completion](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)</span></span>

<span data-ttu-id="a6e3d-147">เมื่อคุณชี้ไปที่วงเล็บที่พิมพ์แล้ว วงเล็บที่สองของคู่นี้จะถูกเน้นโดยอัตโนมัติเพื่อแสดงโครงสร้างที่รองรับ</span><span class="sxs-lookup"><span data-stu-id="a6e3d-147">When you point to the typed bracket, the second bracket of this pair is automatically highlighted to show the construct that they support.</span></span>

## <a name=""></a><span data-ttu-id="a6e3d-148"><a name="CodeNavigation">การนำทางรหัส</a></span><span class="sxs-lookup"><span data-stu-id="a6e3d-148"><a name="CodeNavigation">Code navigation</a></span></span>

<span data-ttu-id="a6e3d-149">คุณสามารถค้นหาตำแหน่งสัญลักษณ์หรือบรรทัดที่ต้องการในนิพจน์ของคุณโดยพิมพ์คำสั่ง **ไปยัง** โดยใช้ชุดคำสั่งหรือเมนูบริบท</span><span class="sxs-lookup"><span data-stu-id="a6e3d-149">You can locate required symbols or lines in your expression by typing the **Go to** command using the command palette or the context menu.</span></span>

<span data-ttu-id="a6e3d-150">ตัวอย่างเช่น เพื่อข้ามไปยังบรรทัด **8** กระทำได้ดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="a6e3d-150">For example, to jump to line **8**, do the following:</span></span>

- <span data-ttu-id="a6e3d-151">กด **Ctrl+G** ป้อนค่า **8** แล้วกด **ป้อน**</span><span class="sxs-lookup"><span data-stu-id="a6e3d-151">Press **Ctrl+G**, enter the value **8**, and then press **Enter**.</span></span>

  <span data-ttu-id="a6e3d-152">หรือ</span><span class="sxs-lookup"><span data-stu-id="a6e3d-152">-or-</span></span>

- <span data-ttu-id="a6e3d-153">กด **F1** พิมพ์ **G** เลือก **ไปยังบรรทัด** ป้อนค่า **8** แล้วกด **ป้อน**</span><span class="sxs-lookup"><span data-stu-id="a6e3d-153">Press **F1**, type **G**, select **Go to line**, enter the value **8**, and the press **Enter**.</span></span>

<span data-ttu-id="a6e3d-154">[![GIF เครื่องมือแก้ไขสูตรขั้นสูง ER ที่แสดงวิธีการระบุที่ตั้งส่วนของนิพจน์โดยใช้ชุดแบบสีของข้อความสั่ง](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)</span><span class="sxs-lookup"><span data-stu-id="a6e3d-154">[![ER formula editor gif showing how to locate parts of an expression using the command palette](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)</span></span>

## <a name=""></a><span data-ttu-id="a6e3d-155"><a name="CodeStructuring">กำหนดโครงสร้างรหัส</a></span><span class="sxs-lookup"><span data-stu-id="a6e3d-155"><a name="CodeStructuring">Code structuring</a></span></span>

<span data-ttu-id="a6e3d-156">รหัสสำหรับฟังก์ชั่นบางอย่าง เช่น [IF](er-functions-logical-if.md) หรือ [CASE](er-functions-logical-case.md) จะถูกจัดโครงสร้างโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="a6e3d-156">The code for some functions, such as [IF](er-functions-logical-if.md) or [CASE](er-functions-logical-case.md), is automatically structured.</span></span> <span data-ttu-id="a6e3d-157">คุณสามารถขยายและยุบขอบเขตที่ซ่อนอยู่ใด ๆ หรือทั้งหมดของรหัสนี้เพื่อลดส่วนที่แก้ไขได้ของนิพจน์ เพื่อเน้นเฉพาะชิ้นส่วนของรหัสที่คุณต้องให้ความสนใจ</span><span class="sxs-lookup"><span data-stu-id="a6e3d-157">You can expand and collapse any or all of the folding regions of this code to reduce the editable part of an expression in order to focus on only  thepiece of code that requires your attention.</span></span> <span data-ttu-id="a6e3d-158">คำสั่งสลับซ่อน/แสดง สามารถใช้สำหรับสิ่งนั้นได้</span><span class="sxs-lookup"><span data-stu-id="a6e3d-158">The toggle fold/unfold commands can be used for that.</span></span>

<span data-ttu-id="a6e3d-159">ตัวอย่างเช่น ซ่อนทุกภูมิภาค กระทำได้ดังต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="a6e3d-159">For example, to fold all regions, do the following:</span></span>

- <span data-ttu-id="a6e3d-160">กด **Ctrl+K**</span><span class="sxs-lookup"><span data-stu-id="a6e3d-160">Press **Ctrl+K**</span></span>

  <span data-ttu-id="a6e3d-161">หรือ</span><span class="sxs-lookup"><span data-stu-id="a6e3d-161">-or-</span></span>

- <span data-ttu-id="a6e3d-162">กด **F1** กด **FO** เลือก **ซ่อนทั้งหมด** แล้วจึงกด **ป้อน**</span><span class="sxs-lookup"><span data-stu-id="a6e3d-162">Press **F1**, press **FO**, select **Fold all**, and then press **Enter**</span></span>

<span data-ttu-id="a6e3d-163">หากต้องการแสดงทุกภูมิภาค ให้ทำดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a6e3d-163">To unfold all regions, do the following:</span></span>

- <span data-ttu-id="a6e3d-164">กด **Ctrl+J**</span><span class="sxs-lookup"><span data-stu-id="a6e3d-164">Press **Ctrl+J**</span></span>

  <span data-ttu-id="a6e3d-165">หรือ</span><span class="sxs-lookup"><span data-stu-id="a6e3d-165">-or-</span></span>
  
- <span data-ttu-id="a6e3d-166">กด **F1** พิมพ์ **UN** เลือก **แสดงทั้งหมด** แล้วจึงกด **ป้อน**</span><span class="sxs-lookup"><span data-stu-id="a6e3d-166">Press **F1**, type **UN**, select **Unfold all**, and then press **Enter**</span></span>

<span data-ttu-id="a6e3d-167">[![GIF เครื่องมือแก้ไขสูตรขั้นสูง ER ที่แสดงรหัสที่แสดง](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)</span><span class="sxs-lookup"><span data-stu-id="a6e3d-167">[![ER formula editor gif showing code being unfolded](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)</span></span>

## <a name=""></a><span data-ttu-id="a6e3d-168"><a name="FindAndReplace">ค้นหาและแทนที่</a></span><span class="sxs-lookup"><span data-stu-id="a6e3d-168"><a name="FindAndReplace">Find and replace</a></span></span>

<span data-ttu-id="a6e3d-169">หากต้องการค้นหาข้อความบางข้อความ ให้เลือกข้อความในนิพจน์ของคุณ แล้วทำดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a6e3d-169">To find occurrences of certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="a6e3d-170">กด **Ctrl+F** แล้วจึงกด **F3** เพื่อค้นหาข้อความที่ปรากฎขึ้นให้เลือกต่อไป หรือกด **Shift+F3** เพื่อค้นหาการเกิดขึ้นก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="a6e3d-170">Press **Ctrl+F** and then press **F3** to find the next occurrence of the selected text, or press **Shift+F3** to find the previous occurrence.</span></span>

  <span data-ttu-id="a6e3d-171">หรือ</span><span class="sxs-lookup"><span data-stu-id="a6e3d-171">-or-</span></span>
  
- <span data-ttu-id="a6e3d-172">กด **F1** พิมพ์ **F** จากนั้นเลือกตัวเลือกที่ต้องการเพื่อค้นหาข้อความที่เลือก</span><span class="sxs-lookup"><span data-stu-id="a6e3d-172">Press **F1**, type **F**, and then select the required option to find the selected text.</span></span>

<span data-ttu-id="a6e3d-173">เพื่อแทนที่ข้อความที่เกิดขึ้นบางข้อความ ให้เลือกข้อความในนิพจน์ของคุณ แล้วทำดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a6e3d-173">To replace occurrences of a certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="a6e3d-174">กด **Ctrl+H**</span><span class="sxs-lookup"><span data-stu-id="a6e3d-174">Press **Ctrl+H**.</span></span> <span data-ttu-id="a6e3d-175">ป้อนข้อความสำรองและเลือกตัวเลือกการแทนที่ เพื่อแทนที่ข้อความที่เลือกหรือข้อความทั้งหมดที่เกิดขึ้นในนิพจน์ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="a6e3d-175">Enter the alternative text and select the replacement option to replace either the selected text or all occurrences of this text in the current expression.</span></span>

  <span data-ttu-id="a6e3d-176">หรือ</span><span class="sxs-lookup"><span data-stu-id="a6e3d-176">-or-</span></span>
  
- <span data-ttu-id="a6e3d-177">กด **F1** พิมพ์ **R** จากนั้นเลือกตัวเลือกที่ต้องการเพื่อแทนที่ข้อความที่เลือก</span><span class="sxs-lookup"><span data-stu-id="a6e3d-177">Press **F1**, type **R**, and then select the required option to replace the selected text.</span></span> <span data-ttu-id="a6e3d-178">ป้อนข้อความสำรองและเลือกตัวเลือกการแทนที่ เพื่อแทนที่ข้อความที่เลือกหรือข้อความทั้งหมดที่เกิดขึ้นในนิพจน์ปัจจุบัน</span><span class="sxs-lookup"><span data-stu-id="a6e3d-178">Enter the alternative text and select the replacement option to replace either the selected text or all occurrences of this text in the current expression.</span></span>

<span data-ttu-id="a6e3d-179">เพื่อเปลี่ยนข้อความที่เกิดขึ้นบางข้อความ ให้เลือกข้อความในนิพจน์ของคุณ แล้วทำดังต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a6e3d-179">To change all occurrences of a certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="a6e3d-180">กด **Ctrl+F2** จากนั้นป้อนข้อความแสดงแทน</span><span class="sxs-lookup"><span data-stu-id="a6e3d-180">Press **Ctrl+F2** and then enter the alternative text.</span></span>

  <span data-ttu-id="a6e3d-181">หรือ</span><span class="sxs-lookup"><span data-stu-id="a6e3d-181">-or-</span></span>
  
- <span data-ttu-id="a6e3d-182">กด **F1** พิมพ์ **C** จากนั้นเลือกตัวเลือกที่ต้องการเพื่อเปลี่ยนข้อความที่เลือก</span><span class="sxs-lookup"><span data-stu-id="a6e3d-182">Press **F1**, type **C**, and then select the required option to change the selected text.</span></span> <span data-ttu-id="a6e3d-183">ป้อนข้อความแสดงแทน</span><span class="sxs-lookup"><span data-stu-id="a6e3d-183">Enter the alternative text.</span></span>

<span data-ttu-id="a6e3d-184">[![GIF เครื่องมือแก้ไขสูตรขั้นสูง ER ที่แสดงการค้นหาและแทนที่](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)</span><span class="sxs-lookup"><span data-stu-id="a6e3d-184">[![ER formula editor gif showing find and replace](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)</span></span>

## <a name=""></a><span data-ttu-id="a6e3d-185"><a name="DataPasting">การวางแหล่งข้อมูลและฟังก์ชั่น</a></span><span class="sxs-lookup"><span data-stu-id="a6e3d-185"><a name="DataPasting">Data sources and functions pasting</a></span></span>

<span data-ttu-id="a6e3d-186">คุณสามารถเลือก **เพิ่มแหล่งข้อมูล** ซึ่งวางไปที่นิพจน์ปัจจุบันซึ่งเป็นแหล่งข้อมูลที่เลือกไว้ในปัจจุบันบนแผงด้านซ้าย **แหล่งข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="a6e3d-186">You can select **Add data source**, which pastes to the current expression a data source that is currently selected on the **Data source** left panel.</span></span> <span data-ttu-id="a6e3d-187">ในทางเดียวกัน คุณสามารถเลือก **เพิ่มฟังก์ชัน** ซึ่งวางไปที่นิพจน์ปัจจุบันซึ่งเป็นฟังก์ชันที่เลือกไว้ในปัจจุบันบนแผงด้านขวา **ฟังก์ชัน**</span><span class="sxs-lookup"><span data-stu-id="a6e3d-187">Simlilarly, you can select **Add function**, which pastes to the current expression a function that is currently selected on the **Functions** right panel.</span></span> <span data-ttu-id="a6e3d-188">หากคุณใช้ตัวแก้ไขสูตร ER ฟังก์ชันที่เลือกหรือแหล่งข้อมูลที่เลือกจะถูกวางไว้ที่ส่วนท้ายของนิพจน์ที่กำหนดค่าไว้เสมอ</span><span class="sxs-lookup"><span data-stu-id="a6e3d-188">If you use the ER formula editor, a selected function or a selected data source will always be pasted to the end of the configured expression.</span></span> <span data-ttu-id="a6e3d-189">เมื่อคุณใช้ตัวแก้ไขสูตร ER ขั้นสูง ฟังก์ชันที่เลือกหรือแหล่งข้อมูลที่เลือกจะสามารถวางไว้ที่ส่วนใดส่วนหนึ่งของนิพจน์ที่กำหนดค่าไว้ได้</span><span class="sxs-lookup"><span data-stu-id="a6e3d-189">When you use the advanced ER formula editor, a selected function or a selected data source can be pasted to any part of the configured expression.</span></span> <span data-ttu-id="a6e3d-190">คุณจะต้องใช้เคอร์เซอร์เพื่อระบุตำแหน่งที่คุณต้องการวางข้อมูล</span><span class="sxs-lookup"><span data-stu-id="a6e3d-190">You will need to use the cursor to specify where you want to paste the data.</span></span>

<span data-ttu-id="a6e3d-191">[![GIF เครื่องมือแก้ไขสูตรขั้นสูง ER ที่แสดงการเพิ่มแหล่งข้อมูลและวางฟังก์ชัน](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)</span><span class="sxs-lookup"><span data-stu-id="a6e3d-191">[![ER formula editor gif showing adding a data source and pasting a function](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)</span></span>

## <a name=""></a><span data-ttu-id="a6e3d-192"><a name="SyntaxColorization">การทำสีที่ไวยากรณ์</a></span><span class="sxs-lookup"><span data-stu-id="a6e3d-192"><a name="SyntaxColorization">Syntax colorization</a></span></span>

<span data-ttu-id="a6e3d-193">ขณะนี้มีการใช้สีที่แตกต่างกันเพื่อเน้นส่วนต่างๆของนิพจน์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a6e3d-193">Currently, different colors are used to highlight the following parts of expressions:</span></span>

- <span data-ttu-id="a6e3d-194">ข้อความในเครื่องหมายวงเล็บคู่ที่สามารถแสดงป้ายชื่อรหัสของค่าคงที่ข้อความ</span><span class="sxs-lookup"><span data-stu-id="a6e3d-194">The text in double brackets that can represent a label ID of a text constant.</span></span>

<span data-ttu-id="a6e3d-195">[![ตัวแก้ไขสูตร ER](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)</span><span class="sxs-lookup"><span data-stu-id="a6e3d-195">[![ER formula editor](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)</span></span>

## <a name="limitations"></a><span data-ttu-id="a6e3d-196">การจำกัด</span><span class="sxs-lookup"><span data-stu-id="a6e3d-196">Limitations</span></span>

<span data-ttu-id="a6e3d-197">ขณะนี้โปรแกรมแก้ไขได้รับการสนับสนุนในเว็บเบราเซอร์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="a6e3d-197">The editor is currently supported in the following web browsers:</span></span>

- <span data-ttu-id="a6e3d-198">Chrome</span><span class="sxs-lookup"><span data-stu-id="a6e3d-198">Chrome</span></span>
- <span data-ttu-id="a6e3d-199">Edge</span><span class="sxs-lookup"><span data-stu-id="a6e3d-199">Edge</span></span>
- <span data-ttu-id="a6e3d-200">Firefox</span><span class="sxs-lookup"><span data-stu-id="a6e3d-200">Firefox</span></span>
- <span data-ttu-id="a6e3d-201">Opera</span><span class="sxs-lookup"><span data-stu-id="a6e3d-201">Opera</span></span>
- <span data-ttu-id="a6e3d-202">Safari</span><span class="sxs-lookup"><span data-stu-id="a6e3d-202">Safari</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a6e3d-203">ทรัพยากรเพิ่มเติม</span><span class="sxs-lookup"><span data-stu-id="a6e3d-203">Additional resources</span></span>

- [<span data-ttu-id="a6e3d-204">ภาพรวมการรายงานทางอิเล็กทรอนิกส์ (ER)</span><span class="sxs-lookup"><span data-stu-id="a6e3d-204">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="a6e3d-205">ตัวออกแบบสูตรในการรายงานทางอิเล็กทรอนิกส์</span><span class="sxs-lookup"><span data-stu-id="a6e3d-205">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)
- [<span data-ttu-id="a6e3d-206">ตัวแก้ไข Monaco</span><span class="sxs-lookup"><span data-stu-id="a6e3d-206">Monaco editor</span></span>](https://microsoft.github.io/monaco-editor)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
