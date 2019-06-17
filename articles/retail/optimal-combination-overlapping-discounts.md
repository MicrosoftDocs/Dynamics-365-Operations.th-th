<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="optimal-combination-overlapping-discounts.md" target-language="th-TH">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>optimal-combination-overlapping-discounts.e4f3cd.e327f652855f898e50f1dd853ae20f3a0ff41d9e.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>e327f652855f898e50f1dd853ae20f3a0ff41d9e</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>e2fb0846fcc6298050a0ec82c302e5eb5254e0b5</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/27/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\optimal-combination-overlapping-discounts.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Determine the optimal combination of overlapping discounts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">กำหนดชุดของส่วนลดที่ซ้อนทับกันที่ดีที่สุด</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>When discounts overlap, you must determine the combination of overlapping discounts that will produce the lowest transaction total or the highest total discount.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เมื่อมีการเหลื่อมกับส่วนลด คุณต้องกำหนดชุดของส่วนลดที่ซ้อนทับกันซึ่งจะให้ผลรวมของธุรกรรมต่ำสุดหรือส่วนลดรวมสูงสุด</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103" restype="x-metadata">
          <source>When the discount amount varies according to the price of the products that are purchased, such as in the common 'Buy 1, get 1 X percent off' (BOGO) retail discount, this process becomes an issue of combinatorial optimization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เมื่อยอดเงินส่วนลดแตกต่างกันไปตามราคาของผลิตภัณฑ์ที่ซื้อ เช่น โดยทั่วไปส่วนลดการขายปลีก 'ซื้อ 1 แถม 1 X เปอร์เซ็นต์ส่วนลด' (BOGO) กระบวนการนี้กลายเป็นปัญหาของการปรับให้เหมาะสมแบบรวม</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Determine the optimal combination of overlapping discounts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">กำหนดชุดของส่วนลดที่ซ้อนทับกันที่ดีที่สุด</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>When discounts overlap, you must determine the combination of overlapping discounts that will produce the lowest transaction total or the highest total discount.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เมื่อมีการเหลื่อมกับส่วนลด คุณต้องกำหนดชุดของส่วนลดที่ซ้อนทับกันซึ่งจะให้ผลรวมของธุรกรรมต่ำสุดหรือส่วนลดรวมสูงสุด</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>When the discount amount varies according to the price of the products that are purchased, such as in the common "Buy 1, get 1 X percent off" (BOGO) retail discount, this process becomes an issue of combinatorial optimization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เมื่อยอดเงินส่วนลดแตกต่างกันไปตามราคาของผลิตภัณฑ์ที่ซื้อ เช่น โดยทั่วไปส่วนลดการขายปลีก "ซื้อ 1 รับ 1 ส่วนลด X เปอร์เซ็นต์" (BOGO) กระบวนการนี้กลายเป็นปัญหาของการปรับให้เหมาะสมแบบรวม</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>This article applies to Microsoft Dynamics AX 2012 R3 with KB 3105973 (released November 2, 2015) or later, and to Microsoft Dynamics 365 for Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">บทความนี้นำไปใช้กับ Microsoft Dynamics AX 2012 R3 ที่มี KB 3105973 (ถูกนำออกใช้ในวันที่ 2 พฤศจิกายน 2015) หรือใหม่กว่า และใช้กับ Microsoft Dynamics 365 for Retail</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>To determine the combination overlapping discounts to apply in a timely manner, we have introduced a method for applying overlapping discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เพื่อกำหนดชุดของส่วนลดที่ซ้อนทับกันให้ใช้ในเวลาเหมาะสม เราได้แนะนำวิธีการสำหรับการใช้ส่วนลดที่ทับซ้อนกัน</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>We call this new method <bpt id="p1">**</bpt>marginal value ranking<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เราเรียกวิธีการใหม่นี้ว่า <bpt id="p1">**</bpt>การจัดอันดับมูลค่ากำไร<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Marginal value ranking is used when the time that is required in order to evaluate the possible combinations of overlapping discounts exceeds a threshold that is configurable on the <bpt id="p1">**</bpt>Retail parameters<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">การจัดอันดับมูลค่ากำไรจะใช้เมื่อเวลาที่ต้องใช้ในการประเมินชุดของส่วนลดที่ซ้อนทับกันที่เป็นไปได้เกินขีดจำกัดที่สามารถตั้งค่าคอนฟิกได้ในหน้า <bpt id="p1">**</bpt>พารามิเตอร์การขายปลีก<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>In the marginal value ranking method, a value is calculated for each overlapping discount by using the discount's value on the shared products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ในวิธีการจัดอันดับมูลค่ากำไร มูลค่าจะถูกคำนวณสำหรับส่วนลดที่ซ้อนทับกันแต่ละรายการโดยใช้มูลค่าของส่วนลดในผลิตภัณฑ์ที่ใช้ร่วมกัน</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The overlapped discounts are then applied from the highest relative value to the lowest relative value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">จากนั้นจะมีการใช้ส่วนลดที่ซ้อนทับกันจากมูลค่าที่สัมพันธ์กันสูงสุดกับมูลค่าที่สัมพันธ์กันต่ำสุด</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>For details about the new method, see the "Marginal value" section, later in this article.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">สำหรับรายละเอียดเกี่ยวกับวิธีการใหม่ ให้ดูที่ส่วน "มูลค่ากำไร" ภายหลังในบทความนี้</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Marginal value ranking isn't used when the discount amounts for a product aren't affected by another product in the transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">การจัดอันดับมูลค่ากำไรไม่ได้ถูกนำมาใช้ เมื่อยอดเงินส่วนลดสำหรับผลิตภัณฑ์ไม่ได้รับผลกระทบจากผลิตภัณฑ์อื่นในธุรกรรม</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>For example, this method isn't used for two simple discounts, or for a simple discount and a single product quantity discount.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ตัวอย่างเช่น วิธีการนี้ไม่ได้ใช้สำหรับส่วนลดปกติสองรายการ หรือสำหรับส่วนลดปกติและส่วนลดปริมาณผลิตภัณฑ์เดียว</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Discount examples</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ตัวอย่างส่วนลด</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>You can create an unlimited number of retail discounts on a common set of products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">คุณสามารถสร้างส่วนลดการขายปลีกได้ไม่จำกัดจำนวนบนชุดทั่วไปของผลิตภัณฑ์</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>However, because there is no limit, performance issues can occur when you try to calculate the discounts that should be used on the various products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">อย่างไรก็ตาม เนื่องจากไม่มีข้อจำกัด ทำให้อาจมีปัญหาด้านประสิทธิภาพเมื่อคุณพยายามที่จะคำนวณส่วนลดที่ควรจะใช้กับผลิตภัณฑ์ต่าง ๆ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>The following examples illustrate this issue in more detail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ตัวอย่างต่อไปนี้แสดงให้เห็นถึงปัญหานี้โดยมีรายละเอียดเพิ่มเติม</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>In example 1, we start with two products and two overlapping discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ในตัวอย่างที่ 1 เราเริ่มต้นด้วยผลิตภัณฑ์สองรายการและส่วนลดที่ซ้อนทับกันสองรายการ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Then, in example 2, we show how the issue evolves as more products are added.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">จากนั้น ในตัวอย่างที่ 2 เราแสดงให้เห็นถึงปัญหาเมื่อมีการเพิ่มผลิตภัณฑ์เพิ่มเติม</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Example 1: Two products and two discounts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ตัวอย่างที่ 1: ผลิตภัณฑ์สองรายการและส่วนลดสองรายการ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>In this example, two products are required in order to qualify for each discount, and the discounts can't be combined.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ในตัวอย่างนี้ จำเป็นต้องมีผลิตภัณฑ์สองรายการเพื่อที่จะได้รับส่วนลดแต่ละรายการ และไม่สามารถรวมส่วนลดได้</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>The discounts in this example are <bpt id="p1">**</bpt>Best price<ept id="p1">**</ept> discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ส่วนลดในตัวอย่างนี้คือส่วนลด <bpt id="p1">**</bpt>ราคาที่ดีที่สุด<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Both products qualify for both discounts.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ผลิตภัณฑ์ทั้งสองมีสิทธิ์ได้รับส่วนลดทั้งสองรายการ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Here are the two discounts.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ต่อไปนี้เป็นส่วนลดสองรายการดังกล่าว</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Example of two Best price discounts</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ตัวอย่างของส่วนลดราคาที่ดีที่สุดสองรายการ</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>For any two products, the better of these two discounts depends on the prices of the two products.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">สำหรับผลิตภัณฑ์ใด ๆ สองรายการ ส่วนลดสองรายการเหล่านี้ที่ดีกว่าขึ้นอยู่กับราคาของผลิตภัณฑ์ทั้งสองรายการ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>When the price of both products is equal or almost equal, discount 1 is better.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เมื่อราคาของผลิตภัณฑ์ทั้งสองเท่ากันหรือใกล้เคียงกัน ส่วนลดที่ 1 จะดีกว่า</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>When the price of one product is significantly less than the price of the other product, discount 2 is better.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เมื่อราคาของผลิตภัณฑ์หนึ่งน้อยกว่าราคาของอีกผลิตภัณฑ์หนึ่งอย่างมาก ส่วนลดที่ 2 จะดีกว่า</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Here is the mathematical rule for evaluating these two discounts against each other.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">นี่คือกฎเชิงคณิตศาสตร์สำหรับการประเมินส่วนลดทั้งสองเหล่านี้เทียบกัน</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Rule for evaluating the discounts</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">กฎสำหรับการประเมินส่วนลด</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>When the price of product 1 is equal to two-thirds of the price of product 2, the two discounts are equal.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">เมื่อราคาของผลิตภัณฑ์ 1 เท่ากับสองในสามของราคาของผลิตภัณฑ์ 2 ส่วนลดทั้งสองจะมีค่าเท่ากัน</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>In this example, the effective discount percentage for discount 1 varies from a few percent (when the prices of the two products are far apart) to a maximum of 25 percent (when the two products have the same price).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ในตัวอย่างนี้ เปอร์เซ็นต์ส่วนลดที่มีผลบังคับใช้สำหรับส่วนลด 1 จะแตกต่างกันตั้งแต่เพียงไม่กี่เปอร์เซ็นต์ (เมื่อราคาของผลิตภัณฑ์ทั้งสองแตกต่างกัน) จนถึงสูงสุด 25 เปอร์เซ็นต์ (เมื่อผลิตภัณฑ์ทั้งสองมีราคาเดียวกัน)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>The effective discount percentage for discount 2 is fixed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เปอร์เซ็นต์ส่วนลดที่มีผลบังคับใช้สำหรับส่วนลด 2 ได้รับการแก้ไขแล้ว</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>It's always 20 percent.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ซึ่งจะเท่ากับ 20 เปอร์เซ็นต์เสมอ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Because the effective discount percentage for discount 1 has a range that can be more than or less than discount 2, the best discount depends on the prices of the two products that must be discounted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เนื่องจากเปอร์เซ็นต์ส่วนลดที่มีผลบังคับใช้สำหรับส่วนลด 1 มีช่วงที่อาจมากกว่าหรือน้อยกว่าส่วนลด 2 ส่วนลดที่ดีที่สุดขึ้นอยู่กับราคาของผลิตภัณฑ์ทั้งสองที่จะต้องได้รับส่วนลด</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>In this example, the calculation is completed quickly, because only two discounts are applied on only two products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ในตัวอย่างนี้ การคำนวณเสร็จสมบูรณ์ได้อย่างรวดเร็วเนื่องจากส่วนลดทั้งสองจะถูกนำไปใช้ในผลิตภัณฑ์สองรายการเท่านั้น</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>There are only two possible combinations: one application of discount 1 or one application of discount 2.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">มีเพียงสองชุดที่เป็นไปได้: แอพลิเคชันหนึ่งของส่วนลด 1 หรืออีกหนึ่งแอพลิเคชันของส่วนลด 2</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>There are no permutations to calculate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ไม่มีการเปลี่ยนลำดับที่จะคำนวณ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>The value of each discount is calculated by using both products, and the best discount is used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ค่าของส่วนลดแต่ละจะถูกคำนวณโดยใช้ผลิตภัณฑ์ทั้งสองและใช้ส่วนลดที่ดีที่สุด</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Example 2: Four products and two discounts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ตัวอย่างที่ 2: ผลิตภัณฑ์สี่รายการและส่วนลดสองรายการ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Next, we will use four products and the same two discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ถัดไป เราจะใช้ผลิตภัณฑ์สี่รายการและส่วนลดสองรายการเหมือนเดิม</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>All four products qualify for both discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ผลิตภัณฑ์ทั้งสี่มีสิทธิ์ได้รับส่วนลดทั้งสองรายการ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>There are twelve possible combinations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">มีชุดที่เป็นไปได้สิบสองแบบ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>In the end, two discounts will be applied to the transaction in one of three combinations: two applications of discount 1, two applications of discount 2, or one application of discount 1 and one application of discount 2.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ในตอนท้าย ส่วนลดสองรายการจะถูกนำมาใช้กับธุรกรรมในหนึ่งในสามชุด: แอพลิเคชันสองรายการของส่วนลด 1 แอพลิเคชันสองรายการของส่วนลด 2 หรือแอพลิเคชันหนึ่งรายการของส่วนลด 1 และแอพลิเคชันหนึ่งรายการของส่วนลด 2</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>To illustrate the possible combinations, we will look at two different sets of four products that have different prices:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เมื่อต้องการแสดงชุดที่เป็นไปได้ เราจะดูที่ผลิตภัณฑ์สี่รายการสองชุดที่มีราคาที่แตกต่างกัน:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>All four products have the same price, $15.00.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ผลิตภัณฑ์ทั้งสี่มีราคาเดียวกันคือ $15.00</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>In this case, the best discount combination is two applications of discount 1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ในกรณีนี้ ชุดส่วนลดที่ดีที่สุดคือ แอพลิเคชันสองรายการของส่วนลด 1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Two products will be full price, and two will be 50 percent off.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ผลิตภัณฑ์สองรายการจะมีราคาเต็ม และอีกสองรายการจะได้รับส่วนลด 50 เปอร์เซ็นต์</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>The discounted total for the transaction is $45 (15 + 15 + 7.50 + 7.50), which is $15 (25 percent) off the undiscounted total of $60.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ส่วนลดรวมสำหรับธุรกรรมคือ $45 (15 + 15 + 7.50 + 7.50) ซึ่งก็คือ $15 (25 เปอร์เซ็นต์) จากจำนวนรวมที่ยังไม่ได้ลดคือ $60</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Discount 2 is only $12 (20 percent).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ส่วนลด 2 คือ $12 เท่านั้น (20 เปอร์เซ็นต์)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Two products are $20 each, one product is $15, and one product is $5.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ผลิตภัณฑ์สองรายการได้รับส่วนลดรายการละ $20 ผลิตภัณฑ์หนึ่งได้รับ $15 และอีกผลิตภัณฑ์หนึ่งได้รับ $5</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>In this case, the best discount combination is one application of discount 2 and one application of discount 1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ในกรณีนี้ ชุดส่วนลดที่ดีที่สุดคือ แอพลิเคชันหนึ่งรายการของส่วนลด 2 และแอพลิเคชันหนึ่งรายการของส่วนลด 1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>The following tables illustrates the discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ตารางต่อไปนี้แสดงส่วนลด</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>To read the tables, use one product from a row and one product from a column.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เมื่อต้องการอ่านตาราง ให้ใช้จากผลิตภัณฑ์หนึ่งจากแถวและอีกหนึ่งผลิตภัณฑ์จากคอลัมน์</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>For example, in the table for discount 1, when you combine the two $20 products, you get $10 off.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ตัวอย่างเช่น ในตารางส่วนลด 1 เมื่อคุณรวมผลิตภัณฑ์ $20 ทั้งสอง คุณจะได้รับส่วนลด $10</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>In the table for discount 2, when you combine the $15 product and the $5 product, you get $4 off.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ในตารางส่วนลด 2 เมื่อคุณรวมผลิตภัณฑ์ $15 และผลิตภัณฑ์ $5 คุณจะได้รับส่วนลด $4</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Example that uses four products for the same two discounts</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ตัวอย่างที่ใช้ผลิตภัณฑ์สี่รายการสำหรับส่วนลดสองรายการที่เหมือนกัน</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>First, we find the largest discount that is available from any two products by using either discount.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ก่อนอื่น เราจะค้นหาส่วนลดที่มากที่สุดที่พร้อมใช้งานจากผลิตภัณฑ์ใด ๆ สองรายการโดยใช้ส่วนลดอย่างใดอย่างหนึ่ง</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>The two tables show the discount amount for all combinations of the two products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ตารางทั้งสองแสดงยอดเงินส่วนลดสำหรับชุดทั้งหมดของผลิตภัณฑ์สองรายการ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>The shaded portions of the tables represent either cases where a product is paired with itself, which we can't do, or a reverse pairing of two products that produces the same discount amount and can be ignored.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ส่วนที่แรเงาของตารางแสดงให้เห็นถึงกรณีที่ผลิตภัณฑ์ถูกจับคู่กับตัวเอง ซึ่งเราไม่สามารถทำได้ หรือย้อนกลับการจับคู่ของผลิตภัณฑ์สองรายการที่ให้ยอดเงินส่วนลดที่เหมือนกัน และสามารถละเว้นได้</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>By looking at the tables, you can see that discount 1 for the two $20 items is the largest discount that is available for either discount on all four products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เมื่อดูที่ตาราง คุณจะเห็นว่าส่วนลด 1 สำหรับสินค้าสองรายการราคา $20 คือส่วนลดที่มากที่สุดที่มีสำหรับส่วนลดของผลิตภัณฑ์ทั้งสี่</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>(This discount is highlighted in green in the first table.) That leaves only the $15 product and the $5 product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(ส่วนลดนี้จะถูกเน้นเป็นสีเขียวในตารางแรก) ที่ให้เฉพาะผลิตภัณฑ์ $15 และผลิตภัณฑ์ $5</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>By looking at the two tables again, you can see that, for these two products, discount 1 gives a $2.50 discount, whereas discount 2 gives a $4 discount.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เมื่อดูที่สองตารางนี้อีกครั้ง คุณจะเห็นว่าสำหรับผลิตภัณฑ์สองรายการนี้ ส่วนลด 1 จะให้ส่วนลด $2.50 ในขณะที่ส่วนลด 2 ให้ส่วนลด $4</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Therefore, we select discount 2.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ดังนั้น เราจะเลือกส่วนลด 2</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>The total discount is $14.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ยอดรวมส่วนลดเท่ากับ $14</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>To make this discussion easier to visualize, here are two additional tables that show the effective discount percentage for all possible two-product combinations for both discount 1 and discount 2.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เพื่อให้มองเห็นภาพของการสนทนานี้ง่ายขึ้น ต่อไปนี้เป็นตารางเพิ่มเติมสองรายการที่แสดงเปอร์เซ็นต์ส่วนลดที่มีผลบังคับใช้สำหรับชุดของผลิตภัณฑ์สองรายการที่เป็นไปได้ทั้งหมดสำหรับทั้งส่วนลด 1 และส่วนลด 2</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Only half the list of combinations is included, because, for these two discounts, the order in which the two products are put into the discount doesn't matter.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">มีการรวมเพียงครึ่งหนึ่งของรายการของชุด เนื่องจากสำหรับส่วนลดสองรายการเหล่านี้ ไม่สำคัญว่าผลิตภัณฑ์ทั้งสองจะอยู่ในลำดับใดในส่วนลด</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>The highest effective discount (25 percent) is highlighted in green, and the lowest effective discount (10 percent) is highlighted in red.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ส่วนลดที่มีผลบังคับใช้สูงสุด (25 เปอร์เซ็นต์) จะถูกเน้นเป็นสีเขียว และส่วนลดที่มีผลบังคับใช้ต่ำสุด (10 เปอร์เซ็นต์) จะถูกเน้นเป็นสีแดง</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Effective discount percentage for all two-product combinations for both discounts</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">เปอร์เซ็นต์ส่วนลดที่มีผลบังคับสำหรับชุดผลิตภัณฑ์ทั้งหมดสองชุดสำหรับส่วนลดทั้งสองรายการ</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>When prices vary, and two or more discount compete, the only way to guarantee the best combination of discounts is to evaluate both discounts and compare them.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">เมื่อราคาแตกต่างกัน และมีส่วนลดอย่างน้อยสองรายการที่ดีกว่า วิธีเดียวที่จะรับประกันชุดของส่วนลดที่ดีที่สุดคือการประเมินส่วนลดทั้งสองรายการและนำมาเปรียบเทียบกัน</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Total possible combinations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ชุดที่เป็นไปได้ทั้งหมด</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>This section continues the example from the previous section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ส่วนนี้ยังคงเป็นตัวอย่างจากส่วนก่อนหน้า</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>We will add more products and another discount, and see how many combinations must be calculated and compared.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เราจะเพิ่มผลิตภัณฑ์เพิ่มเติมและส่วนลดอีกหนึ่งรายการ และดูว่าจำต้องคำนวณและเปรียบเทียบกี่ชุด</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>The following table shows the number of possible discount combinations as the product quantity increases.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ตารางต่อไปนี้แสดงหมายเลขของชุดส่วนลดที่เป็นไปได้โดยเป็นการเพิ่มปริมาณผลิตภัณฑ์</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>The table shows what happens both when there are two overlapping discounts, as in the previous example, and when there are three overlapping discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ตารางแสดงสิ่งที่จะเกิดขึ้นทั้งสองกรณีเมื่อมีส่วนลดที่ซ้อนทับกันสองรายการ ดังในตัวอย่างก่อนหน้านี้ และเมื่อมีส่วนลดที่ซ้อนทับกันสามรายการ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>The number of possible discount combinations that must be evaluated soon exceeds what even a fast computer can calculate and compare quickly enough to be acceptable for retail transactions.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">จำนวนของชุดส่วนลดที่เป็นไปได้ที่จะต้องมีการประเมินในเร็ว ๆ นี้มีมากกว่าจำนวนที่แม้แต่คอมพิวเตอร์ที่รวดเร็วสามารถคำนวณและเปรียบเทียบได้อย่างรวดเร็วเพียงพอที่จะยอมรับได้สำหรับธุรกรรมการขายปลีก</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>Number of possible discount combinations as the product quantity increases</source><target logoport:matchpercent="74" state="translated" state-qualifier="fuzzy-match">หมายเลขของชุดส่วนลดที่เป็นไปได้ เมื่อปริมาณผลิตภัณฑ์เพิ่มขึ้น</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>When even larger quantities or more overlapping discounts are applied, the total number of possible discount combinations quickly goes into the millions, and the time that is required in order to evaluate and select the best possible combination quickly becomes noticeable.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">เมื่อมีการใช้จำนวนที่มากกว่าหรือส่วนลดที่ซ้อนทับกันที่มากกว่า จำนวนรวมของชุดส่วนลดที่เป็นไปได้สามารถเพิ่มขึ้นถึงหลายล้านได้อย่างรวดเร็ว และเวลาที่ต้องใช้ในการประเมินและเลือกชุดที่เป็นไปได้ที่ดีที่สุดได้จะเพิ่มขึ้นอย่างเห็นได้ชัด</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Some optimizations have been done in the retail price engine to reduce the total number of combinations that must be evaluated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">มีการทำการปรับให้เหมาะสมบางอย่างในกลไกจัดการราคาขายปลีกเพื่อลดจำนวนรวมของชุดที่ต้องมีการประเมิน</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>However, because the number overlapping discounts and the quantities in a transaction aren't limited, a large number of combinations will always have to be evaluated whenever there are overlapping discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">อย่างไรก็ตาม เนื่องจากจำนวนของส่วนลดที่ซ้อนทับกันและปริมาณในธุรกรรมไม่ได้ถูกจำกัด ชุดจำนวนมากจะต้องได้รับการประเมินเสมอ เมื่อใดก็ตามที่มีส่วนลดที่ซ้อนทับกัน</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>This issue is the issue that the marginal value ranking method addresses.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ปัญหานี้เป็นปัญหาที่ระบุถึงวิธีการจัดอันดับมูลค่ากำไร</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Marginal value method</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">วิธีคิดมูลค่ากำไร</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>To resolve the issue of an exponentially increasing number of combinations that must be evaluated, an optimization exists that calculates the value per shared product of each discount on the set of products that two or more discounts can be applied to.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เมื่อต้องการแก้ไขปัญหาของการเพิ่มขึ้นแบบยกกำลังของจำนวนชุดที่ต้องมีการประเมิน การปรับให้เหมาะสมมีการคำนวณมูลค่าต่อผลิตภัณฑ์ที่ใช้ร่วมกันของส่วนลดแต่ละรายการบนชุดของผลิตภัณฑ์ที่สามารถใช้กับส่วนลดอย่างน้อยสองรายการ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>We refer to this value as the <bpt id="p1">**</bpt>marginal value<ept id="p1">**</ept> of the discount for the shared products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เราอ้างอิงถึงมูลค่านี้เป็น <bpt id="p1">**</bpt>มูลค่ากำไร<ept id="p1">**</ept> ของส่วนลดสำหรับผลิตภัณฑ์ที่ใช้ร่วมกัน</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>The marginal value is the average per product increase in the total discount amount when the shared products are included in each discount.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">มูลค่ากำไรเป็นค่าเฉลี่ยต่อการเพิ่มของผลิตภัณฑ์ในยอดเงินส่วนลดรวมเมื่อผลิตภัณฑ์ที่ใช้ร่วมกันมีอยู่ในส่วนลดแต่ละรายการ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>The marginal value is calculated by taking the total discount amount (DTotal), subtracting the discount amount without the shared products (DMinus<ph id="ph1">\\</ph> Shared), and dividing that difference by the number of shared products (ProductsShared).</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">มูลค่ากำไรถูกคำนวณด้วยการหักยอดเงินส่วนลดรวม (DTotal) โดยหักยอดเงินส่วนลดโดยไม่มีผลิตภัณฑ์ที่ใช้ร่วมกัน (DMinus<ph id="ph1">\\</ph> ใช้ร่วมกัน) และหารผลต่างนั้นด้วยจำนวนของผลิตภัณฑ์ที่ใช้ร่วมกัน (ProductsShared)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>Formula for calculating marginal value</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">สูตรสำหรับการคำนวณมูลค่ากำไร</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>After the marginal value of each discount on a shared set of products is calculated, the discounts are applied to the shared products in order, exhaustively, from highest marginal value to lowest marginal value.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">หลังจากที่มีการคำนวณมูลค่ากำไรของแต่ละส่วนลดบนชุดของผลิตภัณฑ์ที่ใช้ร่วมกัน ส่วนลดจะถูกนำไปใช้กับผลิตภัณฑ์ที่ใช้ร่วมกันตามใบสั่งจากมูลค่ากำไรสูงสุดถึงมูลค่ากำไรต่ำสุดอย่างละเอียดถี่ถ้วน</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>For this method, all remaining discount possibilities aren't compared every time after a single instance of a discount is applied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">สำหรับวิธีการนี้ ความเป็นไปได้ของส่วนลดที่เหลืออยู่ทั้งหมดจะไม่ถูกเปรียบเทียบทุกครั้งหลังจากที่มีการใช้อินสแตนซ์เดียวของส่วนลด</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>Instead, the overlapping discounts are compared one time and then applied in order.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">แต่ส่วนลดที่ซ้อนทับกันจะถูกเปรียบเทียบหนึ่งครั้ง และถูกนำไปใช้ตามลำดับ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>No additional comparisons are done.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ไม่มีการดำเนินการเปรียบเทียบเพิ่มเติม</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>You can configure the threshold to switch to the marginal value method on the <bpt id="p1">**</bpt>Discount<ept id="p1">**</ept> tab of the <bpt id="p2">**</bpt>Retail parameters<ept id="p2">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">คุณสามารถตั้งค่าคอนฟิกขีดจำกัดให้สลับไปยังวิธีการคิดมูลค่ากำไรบนแท็บ <bpt id="p1">**</bpt>ส่วนลด<ept id="p1">**</ept> ของหน้า <bpt id="p2">**</bpt>พารามิเตอร์การขายปลีก<ept id="p2">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>The acceptable time to calculate the total discount varies across retail industries.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">เวลาที่ยอมรับได้ในการคำนวณส่วนลดรวมแตกต่างกันตามแต่อุตสาหกรรมการขายปลีก</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>However, this time generally falls in the range of tens of milliseconds to one second.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">อย่างไรก็ตาม โดยทั่วไปเวลานี้จะอยู่ในช่วงของมิลลิวินาทีหลักสิบถึงหนึ่งวินาที</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>