<script setup lang="ts">
import type { NuxtError } from '#app'

defineProps<{
  error: NuxtError
}>()

// WeConnect-branded not-found / expired page. Stays on Cloudflare (no redirect to origin).
const homeUrl = 'https://we-connect.co.il'
</script>

<template>
  <div
    dir="rtl"
    style="min-height:100vh;display:flex;align-items:center;justify-content:center;background:#f5f5f6;font-family:Arial,'Helvetica Neue',sans-serif;padding:24px;box-sizing:border-box;"
  >
    <div
      style="max-width:480px;width:100%;text-align:center;background:#fff;border-radius:16px;padding:40px 28px;box-shadow:0 8px 30px rgba(0,0,0,.08);"
    >
      <div style="font-size:28px;font-weight:800;color:#1a1a2e;letter-spacing:-.5px;">
        WeConnect
      </div>
      <div style="font-size:60px;line-height:1;margin:20px 0 6px;">
        🔗
      </div>
      <h1 style="font-size:22px;margin:0 0 10px;color:#1a1a2e;font-weight:700;">
        הקישור לא נמצא
      </h1>
      <p style="color:#666;font-size:15px;line-height:1.6;margin:0 0 26px;">
        ייתכן שהקישור שגוי, הוסר, או שפג תוקפו.
      </p>
      <a
        :href="homeUrl"
        style="display:inline-block;background:#1a1a2e;color:#fff;text-decoration:none;padding:12px 30px;border-radius:10px;font-weight:700;font-size:15px;"
      >
        מעבר לאתר WeConnect
      </a>
    </div>
  </div>
</template>
