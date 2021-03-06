## API

<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

#### Table of Contents

- [class: Plugin](#class-plugin)

### class: [Plugin](https://github.com/berstend/puppeteer-extra/blob/e6133619b051febed630ada35241664eba59b9fa/packages/puppeteer-extra-plugin-stealth/evasions/chrome.csi/index.js#L25-L70)

- `opts` (optional, default `{}`)

**Extends: PuppeteerExtraPlugin**

Mock the `chrome.csi` function if not available (e.g. when running headless).
It's a deprecated (but unfortunately still existing) chrome specific API to fetch browser timings.

Internally chromium switched the implementation to use the WebPerformance API,
so we can do the same to create a fully functional mock. :-)

Note: We're using the deprecated PerformanceTiming API instead of the new Navigation Timing Level 2 API on purpopse.

- **See: <https://bugs.chromium.org/p/chromium/issues/detail?id=113048>**
- **See: <https://codereview.chromium.org/2456293003/>**
- **See: <https://developers.google.com/web/updates/2017/12/chrome-loadtimes-deprecated>**
- **See: <https://developer.mozilla.org/en-US/docs/Web/API/PerformanceTiming>**
- **See: <https://source.chromium.org/chromium/chromium/src/+/master:chrome/renderer/loadtimes_extension_bindings.cc;l=124?q=loadtimes&ss=chromium>**
- **See: `chrome.loadTimes` evasion**

---
