<template>
  <!-- eslint-disable max-len -->
  <main class="container">
    <div class="columns mt-3">
      <div class="col-12 mt-3 text-center">
        <img width="280px" alt="ElegantOTA" src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAzNzQuOTQ1MTQwOTYwNTYxNSA2NC44IiBoZWlnaHQ9IjY0LjgiIHdpZHRoPSIzNzQuOTQ1MTQwOTYwNTYxNSIgc3R5bGU9IndpZHRoOiAzNzQuOTQ1cHg7IGhlaWdodDogNjQuOHB4OyBwb3NpdGlvbjogYWJzb2x1dGU7IHRvcDogNTAlOyBsZWZ0OiA1MCU7IHRyYW5zZm9ybTogdHJhbnNsYXRlKC01MCUsIC01MCUpIHNjYWxlKDAuODgwMTI5KTsgei1pbmRleDogMDsgY3Vyc29yOiBwb2ludGVyOyI+PGRlZnMgaWQ9IlN2Z2pzRGVmczExMDMiPjwvZGVmcz48ZyBpZD0iU3ZnanNHMTEwNCIgZmVhdHVyZWtleT0ibmFtZUxlZnRGZWF0dXJlLTAiIHRyYW5zZm9ybT0ibWF0cml4KDEuMDc2NTU0OTQ1MzI1NzE4NiwwLDAsMS4wNzY1NTQ5NDUzMjU3MTg2LC0zLjQ0NDk3NDU5MzAyMjkzNzYsNy44OTQ3Mzc0NjM1MTg1Mzc0KSIgZmlsbD0iI2Q5NDM0MyI+PHBhdGggZD0iTTMxLjI0IDM4LjI4IGMwLjE2IDAuMjQgMC4yIDAuNTYgMC4xNiAwLjk2IGMtMC4wOCAwLjQ4IC0wLjQ0IDAuOCAtMC45MiAwLjggbC00LjQgMCBjLTAuMzYgMCAtMC42NCAtMC4wOCAtMC44NCAtMC4yNCBjLTAuMTYgLTAuMTIgLTAuMjggLTAuMzIgLTAuNDQgLTAuNTYgbC03LjI0IC0xMi44NCBsLTguNDQgMCBsMCAxMi4yNCBjMCAxLjI0IC0wLjc2IDEuNCAtMS4xMiAxLjQgbC0zLjY0IDAgYy0wLjM2IDAgLTEuMTYgLTAuMTYgLTEuMTYgLTEuNCBsMCAtMTYuOCBjMCAtMS4yNCAwLjggLTEuMzYgMS4xNiAtMS4zNiBsMTcuNCAwIGMxLjA0IDAgMS43MiAtMC4yOCAyLjEyIC0wLjg4IGMwLjQ0IC0wLjYgMC42NCAtMS41NiAwLjY0IC0yLjg4IHMtMC4yIC0yLjI4IC0wLjY0IC0yLjg4IGMtMC40IC0wLjYgLTEuMDggLTAuODggLTIuMTIgLTAuODggbC0xNy40IDAgYy0wLjM2IDAgLTEuMTYgLTAuMTIgLTEuMTYgLTEuMzYgbDAgLTMuMTYgYzAgLTEuMjggMC44IC0xLjQgMS4xNiAtMS40IGwxOC40NCAwIGMyLjcyIDAgNC43MiAwLjg0IDUuOTIgMi41NiBjMS4wOCAxLjY0IDEuNjggMy45NiAxLjc2IDcgbDAgMC4yNCBjLTAuMDggMy4wOCAtMC42OCA1LjQgLTEuNzYgNyBjLTEgMS4zNiAtMi41MiAyLjIgLTQuNDggMi40NCB6IE02NS4wMDkgMzIuODQgYzAuMzYgMCAxLjE2IDAuMTIgMS4xNiAxLjM2IGwwIDQuNCBjMCAxLjI0IC0wLjggMS4zNiAtMS4xNiAxLjM2IGwtMTQuMiAwIGMtMS43NiAwIC0zLjI0IC0wLjIgLTQuNDggLTAuNjggYy0xLjI4IC0wLjQ0IC0yLjMyIC0xLjE2IC0zLjEyIC0yLjIgYy0wLjc2IC0xIC0xLjM2IC0yLjMyIC0xLjcyIC0zLjkyIGMtMC4yOCAtMS4zMiAtMC40OCAtMi45MiAtMC41MiAtNC44IGwwIC0wLjIgbDAuMDggLTUuMDQgYzAuMDggLTAuMzYgMC4yNCAtMC42OCAwLjQ0IC0xIGMwLjU2IC0xIDEuNTYgLTEuNiAyLjcyIC0xLjY4IGwyMC42NCAtMC4wNCBjMC4zMiAwIDEuMTIgMC4xMiAxLjEyIDEuMzYgbDAgMy4xNiBjMCAxLjI0IC0wLjggMS40IC0xLjEyIDEuNCBsLTE3Ljg4IDAgYy0wLjA0IDAgLTAuMDggMi44OCAtMC4wOCAyLjg4IGwwLjA4IDAuNjggYzAuMTIgMC43NiAwLjM2IDEuMzYgMC42OCAxLjggYzAuMzIgMC40IDAuNjggMC42OCAxLjIgMC44OCBjMC41NiAwLjE2IDEuMjQgMC4yOCAyLjA4IDAuMjggbDE0LjA4IDAgeiBNNjUuMDQ5IDYuOTYwMDAwMDAwMDAwMDAxIGMwLjMyIDAgMS4xMiAwLjE2IDEuMTIgMS40IGwwIDMuMTYgYzAgMS4yNCAtMC44IDEuNCAtMS4xMiAxLjQgbC0yMyAtMC4wNCBjLTAuMzIgMCAtMS4wOCAtMC4xMiAtMS4wOCAtMS4zNiBsMCAtMy4xMiBjMCAtMS4yOCAwLjc2IC0xLjQ0IDEuMDggLTEuNDQgbDIzIDAgeiBNOTcuMTM3OTk5OTk5OTk5OTkgMTAuNzYwMDAwMDAwMDAwMDAyIGwxMS4yNCAyNy43MiBjMC4xNiAwLjM2IDAuMiAwLjcyIDAuMTIgMC45NiBjLTAuMDggMC4yIC0wLjI0IDAuNiAtMC44OCAwLjYgbC00LjI4IDAgYy0wLjU2IDAgLTAuOTYgLTAuMzIgLTEuMTYgLTAuODggbC05LjkyIC0yNC43NiBsLTAuMDQgLTAuMDggbC0wLjE2IDAgcy0wLjA0IDAuMDQgLTAuMDggMC4xMiBsLTUuMTIgMTIuOTYgbDQuOTYgMCBjMC41MiAwIDAuOTYgMC4zMiAxLjE2IDAuOCBsMS40NCAzLjU2IGMwLjEyIDAuNCAwLjA4IDAuODQgLTAuMTYgMS4xNiBjLTAuMiAwLjM2IC0wLjYgMC41NiAtMS4wNCAwLjU2IGwtOC43NiAwIGwtMi4yOCA1LjcyIGMtMC4yIDAuNTIgLTAuNiAwLjg0IC0xLjEyIDAuODQgbC00LjQgMCBjLTAuNjQgMCAtMC44NCAtMC4zNiAtMC44OCAtMC42IGMtMC4wOCAtMC4yNCAtMC4wNCAtMC42IDAuMDggLTAuOTYgbDExLjE2IC0yNy43MiBjMC41NiAtMS40NCAxLjE2IC0yLjQgMS43NiAtMi45MiBjMC4xNiAtMC4xMiAwLjM2IC0wLjI4IDAuNiAtMC40IGMwLjggLTAuNTYgMS43NiAtMC44NCAyLjc2IC0wLjg0IGMyLjIgMCA0LjEyIDEuNDggNC43NiAzLjU2IHogTTEzNy43MDcgNy4wMzk5OTk5OTk5OTk5OTkgYzIuNzIgMCA0LjY4IDAuODQgNS44OCAyLjU2IGMxLjE2IDEuNiAxLjcyIDMuOTIgMS43NiA3IGMwIDMuMTYgLTAuNTYgNS41NiAtMS43NiA3LjI0IHMtMy4xNiAyLjUyIC01Ljg4IDIuNTIgbC0xMy42OCAwLjA0IGwwIDEyLjI0IGMwIDEuMjQgLTAuOCAxLjQgLTEuMTIgMS40IGwtMy42OCAwIGMtMC4zMiAwIC0xLjEyIC0wLjE2IC0xLjEyIC0xLjQgbDAgLTE2LjggYzAgLTEuMjQgMC44IC0xLjM2IDEuMTIgLTEuMzYgbDE3LjQ0IDAgYzEgMCAxLjcyIC0wLjI4IDIuMTIgLTAuODggYzAuNDQgLTAuNiAwLjY0IC0xLjU2IDAuNjQgLTIuODggcy0wLjIgLTIuMjggLTAuNjQgLTIuODggYy0wLjQgLTAuNiAtMS4xMiAtMC44OCAtMi4xMiAtMC44OCBsLTE3LjQ0IDAgYy0wLjMyIDAgLTEuMTIgLTAuMTIgLTEuMTIgLTEuMzYgbDAgLTMuMTYgYzAgLTEuMjggMC44IC0xLjQgMS4xMiAtMS40IGwxOC40OCAwIHoiPjwvcGF0aD48L2c+PGcgaWQ9IlN2Z2pzRzExMDUiIGZlYXR1cmVrZXk9ImlubGluZVN5bWJvbEZlYXR1cmUtMCIgdHJhbnNmb3JtPSJtYXRyaXgoMC44NTEyNjUxNDEzNzU2MzI0LDAsMCwwLjg1MTI2NTE0MTM3NTYzMjQsMTYzLjMzMDQ3OTA4Mzc1ODk3LC0xMC4xNjMyNTQ2MzMyOTI1MTQpIiBmaWxsPSIjZDk0MzQzIj48ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPjxwb2x5Z29uIHBvaW50cz0iNzguMjY4LDMyLjE4MSA1Ny41MjEsMzIuMTgxIDQ3LjE0OCw1MC4xNDYgNTcuNTIxLDY4LjExMiA3OC4yNjgsNjguMTEyIDg4LjY0MSw1MC4xNDYgICI+PC9wb2x5Z29uPjxwb2x5Z29uIHBvaW50cz0iMjEuNzMyLDUyLjEyOSAxMS4zNTksNzAuMDk1IDIxLjczMiw4OC4wNjEgNDIuNDc4LDg4LjA2MSA1Mi44NTEsNzAuMDk1IDQyLjQ3OCw1Mi4xMjkgICI+PC9wb2x5Z29uPjxwb2x5Z29uIHBvaW50cz0iNDIuNDc4LDQ3Ljg3MSA1Mi44NTEsMjkuOTA1IDQyLjQ3OCwxMS45MzkgMjEuNzMyLDExLjkzOSAxMS4zNTksMjkuOTA1IDIxLjczMiw0Ny44NzEgICI+PC9wb2x5Z29uPjwvZz48L2c+PGcgaWQ9IlN2Z2pzRzExMDYiIGZlYXR1cmVrZXk9Im5hbWVSaWdodEZlYXR1cmUtMCIgdHJhbnNmb3JtPSJtYXRyaXgoMS4wOTA5MDg5NjQ4MDM0MTEsMCwwLDEuMDkwOTA4OTY0ODAzNDExLDIyOS42NjY1NTA5OTI3Mjg2Miw3LjMyMDAwNTA5MDg4NjMwNykiIGZpbGw9IiNkOTQzNDMiPjxwYXRoIGQ9Ik01NC41NjkgMTcuMjQgYzAgMi40OCAtMC42NCA0LjQ0IC0yIDUuOCBjMS40NCAxLjMyIDIuMiAzLjMyIDIuMiA1Ljk2IGwwIDIuNjggYzAgMS4yNCAtMC4xMiAyLjQgLTAuMzIgMy40IGMtMC4yNCAxLjA0IC0wLjU2IDEuOTIgLTEuMDggMi42NCBjLTAuNDggMC43NiAtMS4xNiAxLjMyIC0yIDEuNzIgYy0wLjggMC40IC0xLjggMC42IC0zIDAuNiBsLTE4IDAgYy0xLjI0IDAgLTIuNCAtMC42NCAtMy4wNCAtMS43MiBjLTAuMiAtMC4zNiAtMC4zNiAtMC44IC0wLjQ0IC0xLjI0IGwwLjA0IC0yNy4zMiBjMC4wOCAtMC4zMiAwLjI0IC0wLjY4IDAuNCAtMSBjMC42IC0wLjk2IDEuNiAtMS42IDIuNzYgLTEuNjggbDAgLTAuMDQgbDE3LjY4IDAgYzIuNDQgMCA0LjIgMC42OCA1LjI0IDIuMDQgYzEuMDQgMS4zMiAxLjU2IDMuMzIgMS41NiA1LjkyIGwwIDIuMjQgeiBNMzIuNzY5IDMzLjg4IGMwIDAuMTYgMC4wNCAwLjIgMC4wNCAwLjIgbDEzLjkyIDAgYzAuOCAwIDEuMzYgLTAuMTYgMS42OCAtMC41MiBzMC40OCAtMSAwLjQ4IC0xLjkyIGwwIC0yLjcyIGMwIC0wLjg4IC0wLjIgLTEuNTIgLTAuNTIgLTEuOTIgYy0wLjM2IC0wLjQgLTEuMDQgLTAuNjQgLTIuMDggLTAuNjQgbC03Ljc2IDAgYy0wLjcyIDAgLTEuMzIgLTAuNTYgLTEuMzIgLTEuMzIgbDAgLTMuMjggYzAgLTAuNzIgMC42IC0xLjMyIDEuMzIgLTEuMzIgbDcuNzYgMCBjMS4wNCAwIDEuNzIgLTAuMiAyLjA0IC0wLjU2IGMwLjM2IC0wLjQgMC41MiAtMSAwLjUyIC0xLjc2IGwwIC0yLjc2IGMwIC0wLjg0IC0wLjE2IC0xLjQ4IC0wLjQ4IC0xLjg0IHMtMC44OCAtMC41NiAtMS42NCAtMC41NiBsLTEzLjg4IDAgYy0wLjA0IDAgLTAuMDggMC4wOCAtMC4wOCAwLjI0IGwwIDIwLjY4IHogTTkxLjUzOCA5Ljk2IGMwLjggMSAxLjM2IDIuMzIgMS43MiAzLjkyIGMwLjMyIDEuNTYgMC41MiAzLjQ4IDAuNTIgNS42OCBsMCA3LjkyIGMwIDIuMjQgLTAuMiA0LjE2IC0wLjUyIDUuNzIgYy0wLjM2IDEuNiAtMC45MiAyLjkyIC0xLjcyIDMuOTYgYy0wLjggMSAtMS44NCAxLjc2IC0zLjEyIDIuMiBjLTEuMjQgMC40NCAtMi43NiAwLjY4IC00LjUyIDAuNjggbC05Ljc2IDAgYy0xLjc2IDAgLTMuMjggLTAuMjQgLTQuNDggLTAuNjggYy0xLjI4IC0wLjQ0IC0yLjMyIC0xLjIgLTMuMTIgLTIuMjQgYy0wLjc2IC0xIC0xLjM2IC0yLjMyIC0xLjcyIC0zLjkyIGMtMC4zNiAtMS41NiAtMC41MiAtMy40OCAtMC41MiAtNS43MiBsMCAtNy45MiBjMCAtMi4yNCAwLjE2IC00LjEyIDAuNTIgLTUuNjggYzAuMzYgLTEuNiAwLjk2IC0yLjkyIDEuNzIgLTMuOTIgYzAuOCAtMSAxLjg0IC0xLjc2IDMuMTIgLTIuMjQgYzEuMjQgLTAuNDQgMi43MiAtMC42OCA0LjQ4IC0wLjY4IGw5Ljc2IDAgYzEuNzYgMCAzLjI4IDAuMjQgNC41MiAwLjY4IGMxLjI4IDAuNDggMi4zMiAxLjI0IDMuMTIgMi4yNCB6IE04Ny44MTggMTguODggYzAgLTEuMTYgLTAuMDQgLTIuMTYgLTAuMiAtMi45NiBjLTAuMTIgLTAuNzYgLTAuMzYgLTEuMzYgLTAuNjggLTEuOCBjLTAuMjggLTAuNCAtMC42OCAtMC42OCAtMS4yIC0wLjg4IGMtMC41MiAtMC4xNiAtMS4yIC0wLjI4IC0yLjA0IC0wLjI4IGwtOS4zNiAwIGMtMC44NCAwIC0xLjUyIDAuMTIgLTIuMDQgMC4yOCBjLTAuNTIgMC4yIC0wLjkyIDAuNDggLTEuMiAwLjg4IGMtMC4zMiAwLjQ0IC0wLjUyIDEuMDQgLTAuNjggMS44IGMtMC4xMiAwLjggLTAuMiAxLjggLTAuMiAyLjk2IGwwIDkuMzIgYzAgMS4xNiAwLjA4IDIuMTYgMC4yIDIuOTYgYzAuMTYgMC43MiAwLjM2IDEuMzYgMC42OCAxLjc2IGMwLjI4IDAuNDQgMC42OCAwLjcyIDEuMiAwLjg4IGMwLjUyIDAuMiAxLjIgMC4yOCAyLjA0IDAuMjggbDkuMzYgMCBjMC44NCAwIDEuNTIgLTAuMDggMi4wNCAtMC4yOCBjMC41MiAtMC4xNiAwLjkyIC0wLjQ0IDEuMiAtMC44OCBjMC4zMiAtMC40IDAuNTYgLTEuMDQgMC42OCAtMS43NiBjMC4xNiAtMC44IDAuMiAtMS44IDAuMiAtMi45NiBsMCAtOS4zMiB6IE0xMjIuMTg3IDIyLjkyIGwxMC43MiAxNS4zMiBjMC4yIDAuMjggMC4zMiAwLjYgMC4yNCAxIGMtMC4wNCAwLjQ4IC0wLjM2IDAuNzYgLTAuODggMC43NiBsLTQuNjQgMCBjLTAuMzIgMCAtMC42IC0wLjA0IC0wLjg0IC0wLjE2IGMtMC4yIC0wLjE2IC0wLjQgLTAuMzYgLTAuNTYgLTAuNjggbC04LjA4IC0xMS40NCBsLTguMTIgMTEuNDggYy0wLjE2IDAuMjggLTAuMzYgMC40OCAtMC41NiAwLjYgYy0wLjIgMC4xNiAtMC40OCAwLjIgLTAuODQgMC4yIGwtNC40IDAgYy0wLjQ4IDAgLTAuOCAtMC4yOCAtMC44OCAtMC43NiBjLTAuMDQgLTAuNCAwLjA0IC0wLjcyIDAuMjggLTEgbDExIC0xNS41NiBsLTkuOTIgLTEzLjg4IGMtMC4yIC0wLjI4IC0wLjI4IC0wLjY0IC0wLjI0IC0xIGMwLjA0IC0wLjQ4IDAuMzYgLTAuNzYgMC44OCAtMC43NiBsNC42NCAwIGMwLjMyIDAgMC42NCAwLjA4IDAuODQgMC4yIGMwLjIgMC4xNiAwLjQgMC4zNiAwLjU2IDAuNiBsNy4wOCAxMC4yNCBsNy41MiAtMTAuMjQgYzAuMTYgLTAuMjQgMC4zNiAtMC40NCAwLjU2IC0wLjYgYzAuMiAtMC4xMiAwLjQ4IC0wLjIgMC44NCAtMC4yIGw0LjQgMCBjMC41MiAwIDAuODQgMC4yOCAwLjkyIDAuNzYgYzAuMDQgMC4zNiAtMC4wNCAwLjcyIC0wLjI4IDEgeiI+PC9wYXRoPjwvZz48L3N2Zz4NCg0K">
      </div>
      <div class="col-12 p-centered"></div>
      <div class="col-12 mt-3 p-centered" v-if="loading">
        <div class="col-3 col-sm-10 p-centered">
          <div class="loading loading-lg mt-3"></div>
        </div>
      </div>
      <transition name="fade" mode="out-in">
        <div class="col-12 mt-3 pt-2 p-centered" v-if="!loading && !uploading && OTAError !== null" key="error">
          <div class="col-3 col-sm-9 col-md-6 p-centered text-center">
            <svg width="32px" height="32px" style="vertical-align: middle;" viewBox="0 0 24 24" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
              <g stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
                <rect id="bound" x="0" y="0" width="24" height="24"></rect>
                <circle id="Oval-5" fill="#DF4759" opacity="0.3" cx="12" cy="12" r="10"></circle>
                <rect id="Rectangle-9" fill="#DF4759" x="11" y="7" width="2" height="8" rx="1"></rect>
                <rect id="Rectangle-9-Copy" fill="#DF4759" x="11" y="16" width="2" height="2" rx="1"></rect>
              </g>
            </svg>
            <span style="vertical-align: middle;" class="ml-2"> {{ OTAError }} </span>
          </div>
        </div>
        <div class="col-12 mt-3 pt-2 p-centered" v-else-if="!loading && !uploading && OTASuccess" key="success">
          <div class="col-3 col-sm-9 col-md-6 p-centered text-center">
            <svg width="32px" height="32px" style="vertical-align: middle;" viewBox="0 0 24 24" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
              <g stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
                <rect id="bound" x="0" y="0" width="24" height="24"></rect>
                <circle id="Oval-5" fill="#42BA96" opacity="0.3" cx="12" cy="12" r="10"></circle>
                <path d="M16.7689447,7.81768175 C17.1457787,7.41393107 17.7785676,7.39211077 18.1823183,7.76894473 C18.5860689,8.1457787 18.6078892,8.77856757 18.2310553,9.18231825 L11.2310553,16.6823183 C10.8654446,17.0740439 10.2560456,17.107974 9.84920863,16.7592566 L6.34920863,13.7592566 C5.92988278,13.3998345 5.88132125,12.7685345 6.2407434,12.3492086 C6.60016555,11.9298828 7.23146553,11.8813212 7.65079137,12.2407434 L10.4229928,14.616916 L16.7689447,7.81768175 Z" id="Path-92" fill="#42BA96"></path>
              </g>
            </svg>
            <span style="vertical-align: middle;" class="ml-2 mb-2"> OTA Success </span>
          </div>
        </div>
        <div class="col-12 mt-3 p-centered" v-else-if="!loading && !uploading" key="otainput">
          <div class="col-3 col-sm-9 col-md-6 p-centered">
            <div class="form-group pt-2 mt-2">
              <label class="form-radio form-inline mr-2">
                <input type="radio" name="firmwaretype" for="firmwaretype" value="firmware" v-model="type"><i class="form-icon"></i> Firmware
              </label>
              <label class="form-radio form-inline ml-2">
                <input type="radio" name="firmwaretype" for="firmwaretype" value="filesystem" v-model="type"><i class="form-icon"></i> Filesystem
              </label>
            </div>
            <div class="form-group pt-2 mt-3">
              <input class="form-input file-input" type="file" ref="file" accept=".bin,.bin.gz" @change="uploadOTA">
            </div>
          </div>
        </div>
      </transition>
      <transition name="fade" mode="out-in">
        <div class="col-12 mt-3 mb-2 pt-2 p-centered" v-if="!loading && uploading">
          <div class="col-2 mt-3 mb-2 col-sm-7 col-md-4 text-right p-centered">
            <div class="bar mt-3 bar-sm">
              <div class="bar-item tooltip" :data-tooltip="progress+'%'" :style="{ width: progress+'%' }"></div>
            </div>
            <div class="pt-2">{{progress}}%</div>
          </div>
        </div>
      </transition>
      <div class="col-12 mt-3 p-centered"></div>
    </div>
    <transition name="fade" mode="out-in">
      <div class="columns mt-3" v-if="!loading">
        <div class="col-12 text-center">
          <span class="label label-rounded mr-2">{{ deviceData.id }}</span> - <span class="label label-rounded label-primary ml-2">{{ deviceData.hardware }}</span>
        </div>
      </div>
    </transition>
    <transition name="slide-fade" mode="out-in" appear>
    </transition>
  </main>
</template>

<script>
export default {
  name: 'App',

  data() {
    return {
      loading: true,
      uploading: false,
      progress: 0,
      OTAError: null,
      OTASuccess: false,

      type: 'firmware',
      files: null,
      deviceData: {
        id: null,
        hardware: null,
      },
    };
  },

  methods: {
    uploadOTA() {
      this.uploading = true;
      const formData = new FormData();
      formData.append(this.type, this.$refs.file.files[0]);
      const request = new XMLHttpRequest();

      request.addEventListener('load', () => {
        // request.response will hold the response from the server
        if (request.status === 200) {
          this.OTASuccess = true;
        } else if (request.status !== 500) {
          this.OTAError = `[HTTP ERROR] ${request.statusText}`;
        } else {
          this.OTAError = request.responseText;
        }
        this.uploading = false;
        this.progress = 0;
      });

      // Upload progress
      request.upload.addEventListener('progress', (e) => {
        this.progress = Math.trunc((e.loaded / e.total) * 100);
      });

      request.withCredentials = true;
      request.open('post', '/update');
      request.send(formData);
    },
  },

  mounted() {
    fetch('/update/identity').then(async (response) => {
      if (response.ok) {
        this.deviceData = await response.json();
        this.loading = false;
      }
    }).catch(() => {

    });
  },

};
</script>

<style lang="scss">
$primary-color: #488EFF;
// Variables and mixins
@import "~spectre.css/src/variables";
@import "~spectre.css/src/mixins";

/*! Spectre.css v#{$version} | MIT License | github.com/picturepan2/spectre */
// Reset and dependencies
@import "~spectre.css/src/normalize";
@import "~spectre.css/src/base";

// Elements
@import "~spectre.css/src/typography";

@import "~spectre.css/src/labels";
@import "~spectre.css/src/tooltips";
@import "~spectre.css/src/cards";
@import "~spectre.css/src/bars";
@import "~spectre.css/src/forms";

@import "~spectre.css/src/layout";

@import "~spectre.css/src/animations";
@import "~spectre.css/src/utilities";

.logo{
  width: 100%;
  max-width: 320px;
}

.card{
  border: 0;
  box-shadow: 0 0.25rem 1rem rgba(48,55,66,.1);
  border-radius: 0.275rem;
}

.label{
  font-size: 0.65rem !important;
}

.file-input{
  border-radius: 0.275rem;
}

.shape{
  position: absolute;
  top: 0;
  right: 0;
  bottom: auto;
  width: 300px;
  opacity: 0.4;
  overflow: hidden;
  z-index: 0;

  @media only screen and (min-width: 425px) {
    width: 140px;
    bottom: 0;
    top: auto;
  }

  @media only screen and (min-width: 768px) {
    width: 240px;
    bottom: auto;
    top: 0;
  }
}

.shape>svg{
  fill: rgba(72,142,255, 0.05);
  transform: scaleY(-1);
}

.coffee-link{
  position: absolute;
  bottom: 0;
  left: 0;
  margin: 1rem;
}

.pt-3{
  padding-top: 32px;
}

.mt-3{
  margin-top: 24px;
}

.fade-enter-active, .fade-leave-active {
  transition: opacity .25s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}

.slide-fade-enter-active {
  transition: all .8s ease;
}
.slide-fade-leave-active {
  transition: all .8s cubic-bezier(1.0, 0.5, 0.8, 1.0);
}
.slide-fade-enter, .slide-fade-leave-to {
  transform: translateY(120px);
  opacity: 1;
}
</style>
