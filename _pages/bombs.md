---
layout: page
permalink: /bombs/
title: Bombs
description: The list of bugs and vulnerabilities found during my research.
nav: true
nav_order: 2
---

<!-- pages/bombs.md -->
<div class="bombs">
<div class="container">
    <h2>Protocol Systems (12 CVEs)</h2>
    <div class="table-responsive">
    <table class="table table-sm table-borderless">
    <tr>
        <th scope="row">CVE-2021-38380 </th>
        <td> 
        Live555 through 1.08 mishandles huge requests for the same MP3 stream, leading to recursion and s stack-based buffer over-read. An attacker can leverage this to launch a DoS attack.
        </td>
        <th>CVSS severity score: 7.5</th>
    </tr>
    <tr>
        <th scope="row">CVE-2021-38381 </th>
        <td> 
        Live555 through 1.08 does not handle MPEG-1 or 2 files properly. Sending two successive RTSP SETUP commands for the same track causes a Use-After-Free and daemon crash.
        </td>
        <th scope="row">CVSS severity score: 6.5</th>
    </tr>
    <tr>
        <th scope="row">CVE-2021-38382 </th>
        <td> 
        Live555 through 1.08 does not handle Matroska and Ogg files properly. Sending two successive RTSP SETUP commands for the same track causes a Use-After-Free and daemon crash.
        </td>
        <th scope="row">CVSS severity score: 6.5</th>
    </tr>
    <tr>
        <th scope="row">CVE-2021-38383 </th>
        <td> 
        OwnTone (aka owntone-server) through 28.1 has a use-after-free in net_bind() in misc.c.
        </td>
        <th scope="row">CVSS severity score: 9.8</th>
    </tr>
    <tr>
        <th scope="row">CVE-2021-39282 </th>
        <td> 
        Live555 through 1.08 has a memory leak in AC3AudioStreamParser for AC3 files.
        </td>
        <th scope="row">CVSS severity score: 7.5</th>
    </tr>
    <tr>
        <th scope="row">CVE-2021-39283 </th>
        <td> 
        Live555 through 1.08 allows an assertion failure and application exit via multiple SETUP and PLAY commands in liveMedia/FramedSource.cpp.
        </td>
        <th scope="row">CVSS severity score: 5.5</th>
    </tr>
    <tr>
        <th scope="row">CVE-2021-41396 </th>
        <td> 
        Live555 through 1.08 does not handle socket connections properly. A huge number of incoming socket connections in a short time invokes the error-handling module, in which a heap-based buffer overflow happens. An attacker can leverage this to launch a DoS attack.
        </td>
        <th scope="row">CVSS severity score: 7.5</th>
    </tr>
    <tr>
        <th scope="row">CVE-2021-41397 </th>
        <td> 
        Live555 through 1.08 does not handle MPEG data properly. Sending specific a command sequence in the MPEG stream leaks 2020 bytes once. An attacker can use this to launch a DoS attack.
        </td>
    </tr>
    <tr>
        <th scope="row">CVE-2021-41687 </th>
        <td> 
        DCMTK through 3.6.6 does not handle memory free properly. The program malloc a heap memory for parsing data, but does not free it when error in parsing. Sending specific requests to the dcmqrdb program incur the memory leak. An attacker can use it to launch a DoS attack.
        </td>
        <th scope="row">CVSS severity score: 7.5</th>
    </tr>
    <tr>
        <th scope="row">CVE-2021-41688 </th>
        <td> 
        DCMTK through 3.6.6 does not handle memory free properly. The object in the program is free but its address is still used in other locations. Sending specific requests to the dcmqrdb program will incur a double free. An attacker can use it to launch a DoS attack.
        </td>
        <th scope="row">CVSS severity score: 7.5</th>
    </tr>
    <tr>
        <th scope="row">CVE-2021-41689 </th>
        <td> 
        DCMTK through 3.6.6 does not handle string copy properly. Sending specific requests to the dcmqrdb program, it would query its database and copy the result even if the result is null, which can incur a head-based overflow. An attacker can use it to launch a DoS attack.
        </td>
        <th scope="row">CVSS severity score: 7.5</th>
    </tr>
    <tr>
        <th scope="row">CVE-2021-41690 </th>
        <td> 
        DCMTK through 3.6.6 does not handle memory free properly. The malloced memory for storing all file information are recorded in a global variable LST and are not freed properly. Sending specific requests to the dcmqrdb program can incur a memory leak. An attacker can use it to launch a DoS attack.
        </td>
        <th scope="row">CVSS severity score: 7.5</th>
    </tr>
    </table>
    </div>
</div>

<div class="container">
	<h2>Database Management Systems (122 bugs)</h2>
	<h3>CockroachDB (28 bugs)</h3>
		<details>
			<summary>sql: support SCRUB on temp tables</summary>
			Link: <a href="https://github.com/cockroachdb/cockroach/issues/83770">https://github.com/cockroachdb/cockroach/issues/83770</a> <br />
		</details>
		<details>
			<summary>Internal Error: Comparison Overload not Found</summary>
			Link: <a href="https://github.com/cockroachdb/cockroach/issues/83792">https://github.com/cockroachdb/cockroach/issues/83792</a> <br />
		</details>
		<details>
			<summary>ERROR: no builtin aggregate for SUM_INT on [unknown]</summary>
			Link: <a href="https://github.com/cockroachdb/cockroach/issues/83874">https://github.com/cockroachdb/cockroach/issues/83874</a> <br />
		</details>
		<details>
			<summary>Crashing by EXPLAIN Statement</summary>
			Link: <a href="https://github.com/cockroachdb/cockroach/issues/83965">https://github.com/cockroachdb/cockroach/issues/83965</a> <br />
		</details>
		<details>
			<summary>Invalid Memory Address Error of Specific SQL Query</summary>
			Link: <a href="https://github.com/cockroachdb/cockroach/issues/83973">https://github.com/cockroachdb/cockroach/issues/83973</a> <br />
		</details>
		<details>
			<summary>Unexpected Error of Unique Index</summary>
			Link: <a href="https://github.com/cockroachdb/cockroach/issues/83976">https://github.com/cockroachdb/cockroach/issues/83976</a> <br />
		</details>
		<details>
			<summary>Crash: panic: RecordingStructured has 30 recordings; expected 1</summary>
			Link: <a href="https://github.com/cockroachdb/cockroach/issues/84056">https://github.com/cockroachdb/cockroach/issues/84056</a> <br />
		</details>
		<details>
			<summary>Unexpected Overflow Error by Huge Interval Value</summary>
			Link: <a href="https://github.com/cockroachdb/cockroach/issues/84154">https://github.com/cockroachdb/cockroach/issues/84154</a> <br />
		</details>
		<details>
			<summary>Inconsistent Case Return Types Decimal Int</summary>
			Link: <a href="https://github.com/cockroachdb/cockroach/issues/85356">https://github.com/cockroachdb/cockroach/issues/85356</a> <br />
		</details>
		<details>
			<summary>No Result Returned by SHOW COLUMN</summary>
			Link: <a href="https://github.com/cockroachdb/cockroach/issues/85388">https://github.com/cockroachdb/cockroach/issues/85388</a> <br />
		</details>
		<details>
			<summary>internal error: no volatility for cast decimal::timestamp</summary>
			Link: <a href="https://github.com/cockroachdb/cockroach/issues/85389">https://github.com/cockroachdb/cockroach/issues/85389</a> <br />
		</details>
		<details>
			<summary>opt: internal error: lookup for ComparisonExpr</summary>
			Link: <a href="https://github.com/cockroachdb/cockroach/issues/85390">https://github.com/cockroachdb/cockroach/issues/85390</a> <br />
		</details>
		<details>
			<summary>opt: internal error: no output column equivalent to 2</summary>
			Link: <a href="https://github.com/cockroachdb/cockroach/issues/85393">https://github.com/cockroachdb/cockroach/issues/85393</a> <br />
		</details>
		<details>
			<summary>Unexpected Error in SHOW COLUMNS</summary>
			Link: <a href="https://github.com/cockroachdb/cockroach/issues/85394">https://github.com/cockroachdb/cockroach/issues/85394</a> <br />
		</details>
		<details>
			<summary>opt: internal error: estimated row count must be non-zero </summary>
			Link: <a href="https://github.com/cockroachdb/cockroach/issues/85499">https://github.com/cockroachdb/cockroach/issues/85499</a> <br />
		</details>
		<details>
			<summary>Unexpected Result by UNION</summary>
			Link: <a href="https://github.com/cockroachdb/cockroach/issues/85502">https://github.com/cockroachdb/cockroach/issues/85502</a> <br />
		</details>
		<details>
			<summary>An Unexpected Error in `CROSS MERGE JOIN`</summary>
			Link: <a href="https://github.com/cockroachdb/cockroach/issues/88104">https://github.com/cockroachdb/cockroach/issues/88104</a> <br />
		</details>
		<details>
			<summary>ERROR: internal error: expected *DInt, found tree.dNull</summary>
			Link: <a href="https://github.com/cockroachdb/cockroach/issues/94264">https://github.com/cockroachdb/cockroach/issues/94264</a> <br />
		</details>
		<details>
			<summary>An Unexpected Error in `CROSS MERGE JOIN`</summary>
			Link: <a href="https://github.com/cockroachdb/cockroach/issues/88104">https://github.com/cockroachdb/cockroach/issues/88104</a> <br />
		</details>
		<details>
			<summary>Potential Issue for Estimated Rows</summary>
			Link: <a href="https://github.com/cockroachdb/cockroach/issues/88455">https://github.com/cockroachdb/cockroach/issues/88455</a> <br />
		</details>
		<details>
			<summary>An Issue of Estimated Rows</summary>
			Link: <a href="https://github.com/cockroachdb/cockroach/issues/89161">https://github.com/cockroachdb/cockroach/issues/89161</a> <br />
		</details>
		<details>
			<summary>Unexpected Estimated Rows in `HAVING` clause</summary>
			Link: <a href="https://github.com/cockroachdb/cockroach/issues/89462">https://github.com/cockroachdb/cockroach/issues/89462</a> <br />
		</details>
		<details>
			<summary>Suspicious Estimated Rows by `OR` </summary>
			Link: <a href="https://github.com/cockroachdb/cockroach/issues/90112">https://github.com/cockroachdb/cockroach/issues/90112</a> <br />
		</details>
		<details>
			<summary>Suspicious Estimated Rows by `DISTINCT`</summary>
			Link: <a href="https://github.com/cockroachdb/cockroach/issues/90113">https://github.com/cockroachdb/cockroach/issues/90113</a> <br />
		</details>
		<details>
			<summary>ERROR: internal error: expected *DInt, found tree.dNull</summary>
			Link: <a href="https://github.com/cockroachdb/cockroach/issues/94264">https://github.com/cockroachdb/cockroach/issues/94264</a> <br />
		</details>
		<details>
			<summary>Integer Overflow with Index Hints</summary>
			Link: <a href="https://github.com/cockroachdb/cockroach/issues/110409">https://github.com/cockroachdb/cockroach/issues/110409</a> <br />
		</details>
		<details>
			<summary>Unexpected Error: overflow during Encode</summary>
			Link: <a href="https://github.com/cockroachdb/cockroach/issues/111473">https://github.com/cockroachdb/cockroach/issues/111473</a> <br />
		</details>
		<details>
			<summary>Unexpected Error for ascii()</summary>
			Link: <a href="https://github.com/cockroachdb/cockroach/issues/111474">https://github.com/cockroachdb/cockroach/issues/111474</a> <br />
		</details>
	<h3>DuckDB (1 bugs)</h3>
		<details>
			<summary>Crash When Creating Index</summary>
			Link: <a href="https://github.com/duckdb/duckdb/issues/4976">https://github.com/duckdb/duckdb/issues/4976</a> <br />
		</details>
	<h3>MariaDB (8 bugs)</h3>
		<details>
			<summary>Unexpected Result by not_null_range_scan</summary>
			Link: <a href="https://jira.mariadb.org/browse/MDEV-32076">https://jira.mariadb.org/browse/MDEV-32076</a> <br />
		</details>
		<details>
			<summary>Unexpected Result by optimize_join_buffer_size</summary>
			Link: <a href="https://jira.mariadb.org/browse/MDEV-32099">https://jira.mariadb.org/browse/MDEV-32099</a> <br />
		</details>
		<details>
			<summary>Unexpected Result by join_cache_hashed</summary>
			Link: <a href="https://jira.mariadb.org/browse/MDEV-32105">https://jira.mariadb.org/browse/MDEV-32105</a> <br />
		</details>
		<details>
			<summary>Unexpected Result by outer_join_with_cache</summary>
			Link: <a href="https://jira.mariadb.org/browse/MDEV-32106">https://jira.mariadb.org/browse/MDEV-32106</a> <br />
		</details>
		<details>
			<summary>Unexpected Result by table_elimination</summary>
			Link: <a href="https://jira.mariadb.org/browse/MDEV-32107">https://jira.mariadb.org/browse/MDEV-32107</a> <br />
		</details>
		<details>
			<summary>Unexpected Result by join_cache_incremental</summary>
			Link: <a href="https://jira.mariadb.org/browse/MDEV-32108">https://jira.mariadb.org/browse/MDEV-32108</a> <br />
		</details>
		<details>
			<summary>Unexpected Result by mrr</summary>
			Link: <a href="https://jira.mariadb.org/browse/MDEV-32143">https://jira.mariadb.org/browse/MDEV-32143</a> <br />
		</details>
		<details>
			<summary>Unexpected Result by join_cache_bka</summary>
			Link: <a href="https://jira.mariadb.org/browse/MDEV-32186">https://jira.mariadb.org/browse/MDEV-32186</a> <br />
		</details>
	<h3>MySQL (9 bugs)</h3>
		<details>
			<summary>Suspicious Estimated Rows</summary>
			Link: <a href="https://bugs.mysql.com/bug.php?id=108833">https://bugs.mysql.com/bug.php?id=108833</a> <br />
		</details>
		<details>
			<summary>Suspicious Estimated Rows by JOIN</summary>
			Link: <a href="https://bugs.mysql.com/bug.php?id=108851">https://bugs.mysql.com/bug.php?id=108851</a> <br />
		</details>
		<details>
			<summary>Suspicious Estimated Rows by DISTINCTROW</summary>
			Link: <a href="https://bugs.mysql.com/bug.php?id=108852">https://bugs.mysql.com/bug.php?id=108852</a> <br />
		</details>
		<details>
			<summary>Unexpected Error: Memory capacity exceeded</summary>
			Link: <a href="https://bugs.mysql.com/bug.php?id=111471">https://bugs.mysql.com/bug.php?id=111471</a> <br />
		</details>
		<details>
			<summary>Unexpected Result by subquery_to_derived</summary>
			Link: <a href="https://bugs.mysql.com/bug.php?id=112243">https://bugs.mysql.com/bug.php?id=112243</a> <br />
		</details>
		<details>
			<summary>Unexpected Result by use_invisible_indexes</summary>
			Link: <a href="https://bugs.mysql.com/bug.php?id=112242">https://bugs.mysql.com/bug.php?id=112242</a> <br />
		</details>
		<details>
			<summary>Unexpected Result by block_nested_loop</summary>
			Link: <a href="https://bugs.mysql.com/bug.php?id=112264">https://bugs.mysql.com/bug.php?id=112264</a> <br />
		</details>
		<details>
			<summary>Unexpected Result by the hint JOIN_ORDER</summary>
			Link: <a href="https://bugs.mysql.com/bug.php?id=112269">https://bugs.mysql.com/bug.php?id=112269</a> <br />
		</details>
		<details>
			<summary>Unexpected Result by NO_BNL</summary>
			Link: <a href="https://bugs.mysql.com/bug.php?id=112296">https://bugs.mysql.com/bug.php?id=112296</a> <br />
		</details>
	<h3>SQLite (28 bugs)</h3>
		<details>
			<summary>An Inconsistent Result Depending on Parenthesization</summary>
			Link: <a href="https://sqlite.org/forum/forumpost/af3d07f908">https://sqlite.org/forum/forumpost/af3d07f908</a> <br />
		</details>
		<details>
			<summary>An Unexpected NULL Column Caused by Where Clause in RIGHT JOIN</summary>
			Link: <a href="https://sqlite.org/forum/forumpost/41cc3851d8">https://sqlite.org/forum/forumpost/41cc3851d8</a> <br />
		</details>
		<details>
			<summary>Rows are Unexpectedly Filtered Out by DISTINCT in RIGHT JOIN</summary>
			Link: <a href="https://sqlite.org/forum/forumpost/c06b10ad7e">https://sqlite.org/forum/forumpost/c06b10ad7e</a> <br />
		</details>
		<details>
			<summary>Expression or Constant in GroupBy Clause</summary>
			Link: <a href="https://sqlite.org/forum/forumpost/2458c5dea2">https://sqlite.org/forum/forumpost/2458c5dea2</a> <br />
		</details>
		<details>
			<summary>Ambiguous Reference Error for Right Join</summary>
			Link: <a href="https://sqlite.org/forum/forumpost/e90a8e6e6f">https://sqlite.org/forum/forumpost/e90a8e6e6f</a> <br />
		</details>
		<details>
			<summary>Unexpected Result by WHERE when Joining Tables</summary>
			Link: <a href="https://sqlite.org/forum/forumpost/687b0bf563">https://sqlite.org/forum/forumpost/687b0bf563</a> <br />
		</details>
		<details>
			<summary>Unexpected Result by WHERE/RIGHT JOIN</summary>
			Link: <a href="https://sqlite.org/forum/forumpost/5cfe08eed6">https://sqlite.org/forum/forumpost/5cfe08eed6</a> <br />
		</details>
		<details>
			<summary>Unexpected Result in Joining Virtual Tables</summary>
			Link: <a href="https://sqlite.org/forum/forumpost/3902c7b833">https://sqlite.org/forum/forumpost/3902c7b833</a> <br />
		</details>
		<details>
			<summary>Unexpected Result by Joining</summary>
			Link: <a href="https://sqlite.org/forum/forumpost/c2554d560b">https://sqlite.org/forum/forumpost/c2554d560b</a> <br />
		</details>
		<details>
			<summary>Unexpected Result by RIGHT JOIN on RTree Tables</summary>
			Link: <a href="https://sqlite.org/forum/forumpost/087de2d9ec">https://sqlite.org/forum/forumpost/087de2d9ec</a> <br />
		</details>
		<details>
			<summary>Unexpected Result by WHERE Again</summary>
			Link: <a href="https://sqlite.org/forum/forumpost/de16c4abe2">https://sqlite.org/forum/forumpost/de16c4abe2</a> <br />
		</details>
		<details>
			<summary>Unexpected Result by RIGHT JOIN</summary>
			Link: <a href="https://sqlite.org/forum/forumpost/206d99a16d">https://sqlite.org/forum/forumpost/206d99a16d</a> <br />
		</details>
		<details>
			<summary>Unexpected Assertion Error in SQLite3MemCompare</summary>
			Link: <a href="https://sqlite.org/forum/forumpost/800eecf5e6">https://sqlite.org/forum/forumpost/800eecf5e6</a> <br />
		</details>
		<details>
			<summary>Unexpected Result by ORDER BY</summary>
			Link: <a href="https://sqlite.org/forum/forumpost/323f86cc30">https://sqlite.org/forum/forumpost/323f86cc30</a> <br />
		</details>
		<details>
			<summary>Unexpected Result by RIGHT JOIN with INDEX</summary>
			Link: <a href="https://sqlite.org/forum/forumpost/c4676c4956">https://sqlite.org/forum/forumpost/c4676c4956</a> <br />
		</details>
		<details>
			<summary>Unexpected Result by JSON</summary>
			Link: <a href="https://sqlite.org/forum/forumpost/3d9caa45cb">https://sqlite.org/forum/forumpost/3d9caa45cb</a> <br />
		</details>
		<details>
			<summary>Unexpected Result by Complicated JOINING</summary>
			Link: <a href="https://sqlite.org/forum/forumpost/eeb8173cf8">https://sqlite.org/forum/forumpost/eeb8173cf8</a> <br />
		</details>
		<details>
			<summary>Assertion `pCur->eCurType==CURTYPE_VTAB' failed</summary>
			Link: <a href="https://sqlite.org/forum/forumpost/dafe0500b0">https://sqlite.org/forum/forumpost/dafe0500b0</a> <br />
		</details>
		<details>
			<summary>Unexpected Result by RIGHT JOIN Again</summary>
			Link: <a href="https://sqlite.org/forum/forumpost/51e6959f61">https://sqlite.org/forum/forumpost/51e6959f61</a> <br />
		</details>
		<details>
			<summary>Unexpected Result by Complicated JOINING Again</summary>
			Link: <a href="https://sqlite.org/forum/forumpost/b40696f501">https://sqlite.org/forum/forumpost/b40696f501</a> <br />
		</details>
		<details>
			<summary>Unexpected Assertion Error in valueFromFunction</summary>
			Link: <a href="https://sqlite.org/forum/forumpost/e3243e07e8">https://sqlite.org/forum/forumpost/e3243e07e8</a> <br />
		</details>
		<details>
			<summary>Unexpected Result by FULL OUTER JOIN</summary>
			Link: <a href="https://sqlite.org/forum/forumpost/5610c17c3d">https://sqlite.org/forum/forumpost/5610c17c3d</a> <br />
		</details>
		<details>
			<summary>Unexpected Expression on ON clause</summary>
			Link: <a href="https://sqlite.org/forum/forumpost/57bdf2217d">https://sqlite.org/forum/forumpost/57bdf2217d</a> <br />
		</details>
		<details>
			<summary>Unexpected Expression Result by FULL OUTER JOIN</summary>
			Link: <a href="https://sqlite.org/forum/forumpost/6650cd40b5">https://sqlite.org/forum/forumpost/6650cd40b5</a> <br />
		</details>
		<details>
			<summary>Unexpected Parse Error</summary>
			Link: <a href="https://sqlite.org/forum/forumpost/1a7fea4651">https://sqlite.org/forum/forumpost/1a7fea4651</a> <br />
		</details>
		<details>
			<summary>Unexpected Assertion Error in whereRangeScanEst</summary>
			Link: <a href="https://sqlite.org/forum/forumpost/c3496cf6b1">https://sqlite.org/forum/forumpost/c3496cf6b1</a> <br />
		</details>
		<details>
			<summary>Unexpected Result by Union</summary>
			Link: <a href="https://sqlite.org/forum/forumpost/174afeae57">https://sqlite.org/forum/forumpost/174afeae57</a> <br />
		</details>
		<details>
			<summary>Assertion `pRec->nField>0 && pRec->nField<=pIdx->nSampleCol' failed.</summary>
			Link: <a href="https://sqlite.org/forum/forumpost/3607259d3c">https://sqlite.org/forum/forumpost/3607259d3c</a> <br />
		</details>
	<h3>TiDB (48 bugs)</h3>
		<details>
			<summary>incorrect unresolved column when using natural join</summary>
			Link: <a href="https://github.com/pingcap/tidb/issues/35522">https://github.com/pingcap/tidb/issues/35522</a> <br />
		</details>
		<details>
			<summary>unexpected unresolved column error when the view refers to dual table</summary>
			Link: <a href="https://github.com/pingcap/tidb/issues/35527">https://github.com/pingcap/tidb/issues/35527</a> <br />
		</details>
		<details>
			<summary>Runtime error: invalid memory address</summary>
			Link: <a href="https://github.com/pingcap/tidb/issues/35623">https://github.com/pingcap/tidb/issues/35623</a> <br />
		</details>
		<details>
			<summary>Unexpected Result with a FALSE Expression in WHERE</summary>
			Link: <a href="https://github.com/pingcap/tidb/issues/35645">https://github.com/pingcap/tidb/issues/35645</a> <br />
		</details>
		<details>
			<summary>Unexpected Error by CAST and CHAR functions</summary>
			Link: <a href="https://github.com/pingcap/tidb/issues/35652">https://github.com/pingcap/tidb/issues/35652</a> <br />
		</details>
		<details>
			<summary>Unexpected Error for Function INET_ATON</summary>
			Link: <a href="https://github.com/pingcap/tidb/issues/35677">https://github.com/pingcap/tidb/issues/35677</a> <br />
		</details>
		<details>
			<summary>Unexpected Connection Lost</summary>
			Link: <a href="https://github.com/pingcap/tidb/issues/35678">https://github.com/pingcap/tidb/issues/35678</a> <br />
		</details>
		<details>
			<summary>Inconsistent Results in SELECT</summary>
			Link: <a href="https://github.com/pingcap/tidb/issues/36853">https://github.com/pingcap/tidb/issues/36853</a> <br />
		</details>
		<details>
			<summary>Unexpected Result by CONCAT_WS</summary>
			Link: <a href="https://github.com/pingcap/tidb/issues/36888">https://github.com/pingcap/tidb/issues/36888</a> <br />
		</details>
		<details>
			<summary>ERROR 8141 (HY000): assertion failed</summary>
			Link: <a href="https://github.com/pingcap/tidb/issues/38295">https://github.com/pingcap/tidb/issues/38295</a> <br />
		</details>
		<details>
			<summary>Incorrect Results by `REGEXP`</summary>
			Link: <a href="https://github.com/pingcap/tidb/issues/38303">https://github.com/pingcap/tidb/issues/38303</a> <br />
		</details>
		<details>
			<summary>Incorrect Result by `LEFT JOIN`</summary>
			Link: <a href="https://github.com/pingcap/tidb/issues/38304">https://github.com/pingcap/tidb/issues/38304</a> <br />
		</details>
		<details>
			<summary>runtime error: invalid memory address or nil pointer dereference</summary>
			Link: <a href="https://github.com/pingcap/tidb/issues/38305">https://github.com/pingcap/tidb/issues/38305</a> <br />
		</details>
		<details>
			<summary>Unexpected Results</summary>
			Link: <a href="https://github.com/pingcap/tidb/issues/38310">https://github.com/pingcap/tidb/issues/38310</a> <br />
		</details>
		<details>
			<summary>Error [types:1690]%s value is out of range in '%s'</summary>
			Link: <a href="https://github.com/pingcap/tidb/issues/38352">https://github.com/pingcap/tidb/issues/38352</a> <br />
		</details>
		<details>
			<summary>Unexpected Error: Failed to read auto-increment value from storage engine</summary>
			Link: <a href="https://github.com/pingcap/tidb/issues/38483">https://github.com/pingcap/tidb/issues/38483</a> <br />
		</details>
		<details>
			<summary>Unexpected Results by RIGHT JOIN</summary>
			Link: <a href="https://github.com/pingcap/tidb/issues/38654">https://github.com/pingcap/tidb/issues/38654</a> <br />
		</details>
		<details>
			<summary>rule PredicatePushDown pushes wrong filter across projection</summary>
			Link: <a href="https://github.com/pingcap/tidb/issues/38736">https://github.com/pingcap/tidb/issues/38736</a> <br />
		</details>
		<details>
			<summary>ERROR 8141 (HY000): assertion failed</summary>
			Link: <a href="https://github.com/pingcap/tidb/issues/38295">https://github.com/pingcap/tidb/issues/38295</a> <br />
		</details>
		<details>
			<summary>Incorrect Results by `REGEXP`</summary>
			Link: <a href="https://github.com/pingcap/tidb/issues/38303">https://github.com/pingcap/tidb/issues/38303</a> <br />
		</details>
		<details>
			<summary>Incorrect Result by `LEFT JOIN`</summary>
			Link: <a href="https://github.com/pingcap/tidb/issues/38304">https://github.com/pingcap/tidb/issues/38304</a> <br />
		</details>
		<details>
			<summary>runtime error: invalid memory address or nil pointer dereference</summary>
			Link: <a href="https://github.com/pingcap/tidb/issues/38305">https://github.com/pingcap/tidb/issues/38305</a> <br />
		</details>
		<details>
			<summary>Unexpected Results</summary>
			Link: <a href="https://github.com/pingcap/tidb/issues/38310">https://github.com/pingcap/tidb/issues/38310</a> <br />
		</details>
		<details>
			<summary>Unexpected Estimated Rows of `OR`</summary>
			Link: <a href="https://github.com/pingcap/tidb/issues/38319">https://github.com/pingcap/tidb/issues/38319</a> <br />
		</details>
		<details>
			<summary>Error [types:1690]%s value is out of range in '%s'</summary>
			Link: <a href="https://github.com/pingcap/tidb/issues/38352">https://github.com/pingcap/tidb/issues/38352</a> <br />
		</details>
		<details>
			<summary>Question About the Estimated Rows in `GROUP BY`</summary>
			Link: <a href="https://github.com/pingcap/tidb/issues/38474">https://github.com/pingcap/tidb/issues/38474</a> <br />
		</details>
		<details>
			<summary>Suspicious Estimated Rows by `JOIN`</summary>
			Link: <a href="https://github.com/pingcap/tidb/issues/38479">https://github.com/pingcap/tidb/issues/38479</a> <br />
		</details>
		<details>
			<summary>Suspicious Estimated Rows by HAVING</summary>
			Link: <a href="https://github.com/pingcap/tidb/issues/38482">https://github.com/pingcap/tidb/issues/38482</a> <br />
		</details>
		<details>
			<summary>Unexpected Error: Failed to read auto-increment value from storage engine</summary>
			Link: <a href="https://github.com/pingcap/tidb/issues/38483">https://github.com/pingcap/tidb/issues/38483</a> <br />
		</details>
		<details>
			<summary>Unexpected Results by RIGHT JOIN</summary>
			Link: <a href="https://github.com/pingcap/tidb/issues/38654">https://github.com/pingcap/tidb/issues/38654</a> <br />
		</details>
		<details>
			<summary>Unexpected Estimated Rows by INNER JOIN</summary>
			Link: <a href="https://github.com/pingcap/tidb/issues/38665">https://github.com/pingcap/tidb/issues/38665</a> <br />
		</details>
		<details>
			<summary>Unexpected Estimated Rows by WHERE clause</summary>
			Link: <a href="https://github.com/pingcap/tidb/issues/38721">https://github.com/pingcap/tidb/issues/38721</a> <br />
		</details>
		<details>
			<summary>rule PredicatePushDown pushes wrong filter across projection</summary>
			Link: <a href="https://github.com/pingcap/tidb/issues/38736">https://github.com/pingcap/tidb/issues/38736</a> <br />
		</details>
		<details>
			<summary>runtime error: index out of range [7] with length 4</summary>
			Link: <a href="https://github.com/pingcap/tidb/issues/44747">https://github.com/pingcap/tidb/issues/44747</a> <br />
		</details>
		<details>
			<summary>runtime error: index out of range [0] with length 0</summary>
			Link: <a href="https://github.com/pingcap/tidb/issues/46535">https://github.com/pingcap/tidb/issues/46535</a> <br />
		</details>
		<details>
			<summary>ERROR 1690: overflows float</summary>
			Link: <a href="https://github.com/pingcap/tidb/issues/46538">https://github.com/pingcap/tidb/issues/46538</a> <br />
		</details>
		<details>
			<summary>ERROR 1105 (HY000): interface conversion</summary>
			Link: <a href="https://github.com/pingcap/tidb/issues/46556">https://github.com/pingcap/tidb/issues/46556</a> <br />
		</details>
		<details>
			<summary>Uncertain Results by MERGE_JOIN</summary>
			Link: <a href="https://github.com/pingcap/tidb/issues/46580">https://github.com/pingcap/tidb/issues/46580</a> <br />
		</details>
		<details>
			<summary>Error For MPP Stream</summary>
			Link: <a href="https://github.com/pingcap/tidb/issues/46598">https://github.com/pingcap/tidb/issues/46598</a> <br />
		</details>
		<details>
			<summary>Unexpected Results in TiFlash</summary>
			Link: <a href="https://github.com/pingcap/tidb/issues/46599">https://github.com/pingcap/tidb/issues/46599</a> <br />
		</details>
		<details>
			<summary>Unexpected Results in TiFlash 2</summary>
			Link: <a href="https://github.com/pingcap/tidb/issues/46601">https://github.com/pingcap/tidb/issues/46601</a> <br />
		</details>
		<details>
			<summary>Unexpected Results by the hint USE_INDEX in TiFlash</summary>
			Link: <a href="https://github.com/pingcap/tidb/issues/47019">https://github.com/pingcap/tidb/issues/47019</a> <br />
		</details>
		<details>
			<summary>Unexpected Result by BROADCAST_JOIN in TiFlash</summary>
			Link: <a href="https://github.com/pingcap/tidb/issues/47020">https://github.com/pingcap/tidb/issues/47020</a> <br />
		</details>
		<details>
			<summary>Unexpected Result in TiFlash 3</summary>
			Link: <a href="https://github.com/pingcap/tidb/issues/47286">https://github.com/pingcap/tidb/issues/47286</a> <br />
		</details>
		<details>
			<summary>Unexpected Result by MERGE_JOIN</summary>
			Link: <a href="https://github.com/pingcap/tidb/issues/47345">https://github.com/pingcap/tidb/issues/47345</a> <br />
		</details>
		<details>
			<summary>ERROR 1105 encoding failed</summary>
			Link: <a href="https://github.com/pingcap/tidb/issues/47346">https://github.com/pingcap/tidb/issues/47346</a> <br />
		</details>
		<details>
			<summary>Unexpected Error Lost Connection</summary>
			Link: <a href="https://github.com/pingcap/tidb/issues/47347">https://github.com/pingcap/tidb/issues/47347</a> <br />
		</details>
		<details>
			<summary>Unexpected Error Overflow</summary>
			Link: <a href="https://github.com/pingcap/tidb/issues/47348">https://github.com/pingcap/tidb/issues/47348</a> <br />
		</details>
</div>
