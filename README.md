/* =========================================================
   PARTH PATEL (PP) - CREATOR / ADMIN STUDIO STYLESHEET
   Password Protected Portal: 92655
   ========================================================= */

@import url('https://fonts.googleapis.com/css2?family=Cinzel:wght@500;700;900&family=Outfit:wght@400;500;600;700&family=Plus+Jakarta+Sans:wght@400;500;600;700&display=swap');

:root {
  --admin-gold: #D4AF37;
  --admin-gold-light: #FFF2A6;
  --admin-gold-dark: #A27B17;
  --admin-gold-grad: linear-gradient(135deg, #FFF2A6 0%, #D4AF37 50%, #A27B17 100%);
  
  --admin-bg: #0A0B0E;
  --admin-sidebar-bg: #0F1117;
  --admin-card: #151722;
  --admin-card-hover: #1C2030;
  --admin-input: #1A1E2B;
  
  --text-main: #F3F4F6;
  --text-sub: #9CA3AF;
  --text-dim: #6B7280;

  --border-subtle: rgba(212, 175, 55, 0.2);
  --border-glow: rgba(212, 175, 55, 0.6);
  --border-panel: rgba(255, 255, 255, 0.08);

  --status-pending: #F59E0B;
  --status-processing: #3B82F6;
  --status-shipped: #8B5CF6;
  --status-delivered: #10B981;
  --status-cancelled: #EF4444;
}

body.admin-body {
  font-family: 'Plus Jakarta Sans', sans-serif;
  background-color: var(--admin-bg);
  color: var(--text-main);
  min-height: 100vh;
  margin: 0;
  display: flex;
  flex-direction: column;
}

/* =========================================================
   ADMIN LOGIN GATE (PASSWORD: 92655)
   ========================================================= */
.admin-login-fullscreen {
  position: fixed;
  inset: 0;
  background: radial-gradient(circle at center, #141724 0%, #08090C 100%);
  display: flex;
  align-items: center;
  justify-content: center;
  z-index: 9999;
  padding: 20px;
}

.admin-login-card {
  background: var(--admin-card);
  border: 1px solid var(--border-glow);
  border-radius: 20px;
  width: 100%;
  max-width: 440px;
  padding: 40px 32px;
  box-shadow: 0 20px 60px rgba(0, 0, 0, 0.8), 0 0 40px rgba(212, 175, 55, 0.2);
  text-align: center;
  position: relative;
  overflow: hidden;
}

.admin-login-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 4px;
  background: var(--admin-gold-grad);
}

.admin-login-logo {
  width: 80px;
  height: 80px;
  margin: 0 auto 16px;
  filter: drop-shadow(0 0 12px rgba(212, 175, 55, 0.4));
}

.admin-login-title {
  font-family: 'Cinzel', serif;
  font-size: 1.5rem;
  background: var(--admin-gold-grad);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  margin-bottom: 6px;
}

.admin-login-subtitle {
  font-size: 0.85rem;
  color: var(--text-sub);
  margin-bottom: 24px;
}

.admin-pass-hint {
  background: rgba(212, 175, 55, 0.1);
  border: 1px dashed var(--border-subtle);
  border-radius: 8px;
  padding: 10px;
  font-size: 0.82rem;
  color: var(--admin-gold-light);
  margin-bottom: 20px;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 8px;
}

.admin-login-form .form-group {
  text-align: left;
  margin-bottom: 18px;
}

.admin-login-btn {
  width: 100%;
  background: var(--admin-gold-grad);
  color: #000;
  border: none;
  padding: 14px;
  border-radius: 30px;
  font-family: 'Outfit', sans-serif;
  font-size: 1rem;
  font-weight: 700;
  cursor: pointer;
  box-shadow: 0 4px 20px rgba(212, 175, 55, 0.3);
  transition: transform 0.2s, box-shadow 0.2s;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 8px;
}

.admin-login-btn:hover {
  transform: translateY(-2px);
  box-shadow: 0 8px 30px rgba(212, 175, 55, 0.5);
}

.back-to-store-link {
  display: inline-block;
  margin-top: 18px;
  color: var(--text-dim);
  font-size: 0.85rem;
  text-decoration: none;
  transition: color 0.2s;
}
.back-to-store-link:hover {
  color: var(--admin-gold-light);
}

/* =========================================================
   ADMIN DASHBOARD LAYOUT
   ========================================================= */
.admin-layout {
  display: flex;
  min-height: 100vh;
}

/* Sidebar */
.admin-sidebar {
  width: 270px;
  background: var(--admin-sidebar-bg);
  border-right: 1px solid var(--border-panel);
  display: flex;
  flex-direction: column;
  position: sticky;
  top: 0;
  height: 100vh;
  z-index: 50;
}

.sidebar-header {
  padding: 24px 20px;
  border-bottom: 1px solid var(--border-panel);
  display: flex;
  align-items: center;
  gap: 12px;
}

.sidebar-logo {
  width: 44px;
  height: 44px;
}

.sidebar-brand-name {
  font-family: 'Cinzel', serif;
  font-size: 1.1rem;
  font-weight: 900;
  color: var(--admin-gold-light);
  line-height: 1.1;
}

.sidebar-brand-role {
  font-size: 0.7rem;
  color: var(--text-dim);
  text-transform: uppercase;
  letter-spacing: 1.5px;
}

.sidebar-menu {
  list-style: none;
  padding: 20px 12px;
  display: flex;
  flex-direction: column;
  gap: 6px;
  flex: 1;
}

.sidebar-item-btn {
  width: 100%;
  display: flex;
  align-items: center;
  gap: 14px;
  padding: 12px 16px;
  background: none;
  border: none;
  color: var(--text-sub);
  font-family: 'Outfit', sans-serif;
  font-size: 0.95rem;
  font-weight: 500;
  border-radius: 10px;
  cursor: pointer;
  transition: all 0.2s ease;
  text-align: left;
}

.sidebar-item-btn:hover {
  background: var(--admin-card);
  color: var(--admin-gold-light);
}

.sidebar-item-btn.active {
  background: rgba(212, 175, 55, 0.12);
  color: var(--admin-gold-light);
  border-left: 3px solid var(--admin-gold);
  font-weight: 700;
}

.sidebar-footer {
  padding: 20px 16px;
  border-top: 1px solid var(--border-panel);
  display: flex;
  flex-direction: column;
  gap: 8px;
}

.store-live-btn {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 8px;
  background: rgba(255, 255, 255, 0.05);
  border: 1px solid var(--border-panel);
  color: var(--text-main);
  padding: 10px;
  border-radius: 8px;
  text-decoration: none;
  font-size: 0.88rem;
  font-weight: 600;
  transition: background 0.2s;
}
.store-live-btn:hover {
  background: rgba(212, 175, 55, 0.15);
  color: var(--admin-gold-light);
}

.admin-logout-btn {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 8px;
  background: rgba(239, 68, 68, 0.1);
  border: 1px solid rgba(239, 68, 68, 0.2);
  color: #EF4444;
  padding: 10px;
  border-radius: 8px;
  font-size: 0.88rem;
  font-weight: 600;
  cursor: pointer;
  transition: background 0.2s;
}
.admin-logout-btn:hover {
  background: rgba(239, 68, 68, 0.2);
}

/* =========================================================
   MAIN CONTENT VIEW
   ========================================================= */
.admin-main {
  flex: 1;
  padding: 30px 40px;
  overflow-y: auto;
  max-width: 1400px;
}

.admin-top-bar {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 30px;
}

.admin-view-title h1 {
  font-family: 'Cinzel', serif;
  font-size: 1.8rem;
  color: #fff;
}

.admin-view-title p {
  color: var(--text-sub);
  font-size: 0.88rem;
}

.creator-status-badge {
  background: rgba(16, 185, 129, 0.1);
  border: 1px solid rgba(16, 185, 129, 0.3);
  color: #10B981;
  padding: 6px 14px;
  border-radius: 20px;
  font-size: 0.8rem;
  font-weight: 600;
  display: flex;
  align-items: center;
  gap: 8px;
}

.creator-status-badge::before {
  content: '';
  width: 8px;
  height: 8px;
  border-radius: 50%;
  background: #10B981;
  box-shadow: 0 0 8px #10B981;
}

/* Statistics Metrics Grid */
.admin-metrics-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 20px;
  margin-bottom: 36px;
}

.metric-card {
  background: var(--admin-card);
  border: 1px solid var(--border-panel);
  border-radius: 14px;
  padding: 20px;
  display: flex;
  align-items: center;
  gap: 16px;
  transition: transform 0.2s, border-color 0.2s;
}

.metric-card:hover {
  border-color: var(--admin-gold);
  transform: translateY(-3px);
}

.metric-icon-box {
  width: 52px;
  height: 52px;
  border-radius: 12px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.4rem;
}

.metric-icon-gold {
  background: rgba(212, 175, 55, 0.15);
  color: var(--admin-gold-light);
  border: 1px solid var(--border-subtle);
}
.metric-icon-blue {
  background: rgba(59, 130, 246, 0.15);
  color: #60A5FA;
}
.metric-icon-green {
  background: rgba(16, 185, 129, 0.15);
  color: #34D399;
}
.metric-icon-purple {
  background: rgba(139, 92, 246, 0.15);
  color: #A78BFA;
}

.metric-value {
  font-family: 'Outfit', sans-serif;
  font-size: 1.6rem;
  font-weight: 700;
  color: #fff;
  line-height: 1.2;
}

.metric-label {
  font-size: 0.8rem;
  color: var(--text-sub);
}

/* Tab Panels */
.tab-content-panel {
  display: none;
}
.tab-content-panel.active {
  display: block;
  animation: fadeIn 0.3s ease;
}

@keyframes fadeIn {
  from { opacity: 0; transform: translateY(8px); }
  to { opacity: 1; transform: translateY(0); }
}

/* =========================================================
   ADD NEW CLOTHING ITEM FORM
   ========================================================= */
.add-product-panel {
  background: var(--admin-card);
  border: 1px solid var(--border-panel);
  border-radius: 16px;
  padding: 32px;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
}

.form-header-row {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding-bottom: 20px;
  border-bottom: 1px solid var(--border-panel);
  margin-bottom: 24px;
}

.form-header-row h3 {
  font-family: 'Cinzel', serif;
  font-size: 1.4rem;
  color: var(--admin-gold-light);
}

.add-product-grid {
  display: grid;
  grid-template-columns: 1.2fr 0.8fr;
  gap: 36px;
}

.image-uploader-card {
  background: var(--admin-input);
  border: 2px dashed var(--border-subtle);
  border-radius: 14px;
  padding: 24px;
  text-align: center;
  cursor: pointer;
  transition: border-color 0.2s;
  position: relative;
}

.image-uploader-card:hover {
  border-color: var(--admin-gold);
}

.img-preview-box {
  width: 100%;
  height: 280px;
  border-radius: 10px;
  overflow: hidden;
  margin-bottom: 16px;
  background: #10121A;
  display: flex;
  align-items: center;
  justify-content: center;
}

.img-preview-box img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  display: none;
}

.img-preview-placeholder {
  color: var(--text-dim);
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 8px;
}
.img-preview-placeholder i {
  font-size: 2.8rem;
  color: var(--admin-gold);
}

.sample-images-row {
  display: flex;
  gap: 8px;
  margin-top: 12px;
  overflow-x: auto;
  padding-bottom: 6px;
}

.sample-img-thumb {
  width: 50px;
  height: 50px;
  border-radius: 6px;
  object-fit: cover;
  border: 1px solid var(--border-panel);
  cursor: pointer;
  opacity: 0.7;
  transition: all 0.2s;
}

.sample-img-thumb:hover, .sample-img-thumb.active {
  opacity: 1;
  border-color: var(--admin-gold);
  transform: scale(1.08);
}

.size-checkbox-wrap {
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
}

.size-check-label {
  background: var(--admin-input);
  border: 1px solid var(--border-panel);
  padding: 6px 14px;
  border-radius: 6px;
  font-size: 0.85rem;
  cursor: pointer;
  user-select: none;
  transition: all 0.2s;
}

.size-check-label input {
  display: none;
}

.size-check-label.selected {
  background: var(--admin-gold-grad);
  color: #000;
  font-weight: 700;
  border-color: transparent;
}

.btn-publish-product {
  background: var(--admin-gold-grad);
  color: #000;
  border: none;
  padding: 16px 36px;
  border-radius: 30px;
  font-family: 'Outfit', sans-serif;
  font-size: 1.05rem;
  font-weight: 700;
  cursor: pointer;
  display: flex;
  align-items: center;
  gap: 10px;
  box-shadow: 0 6px 25px rgba(212, 175, 55, 0.4);
  transition: transform 0.2s, box-shadow 0.2s;
}

.btn-publish-product:hover {
  transform: translateY(-3px);
  box-shadow: 0 10px 35px rgba(212, 175, 55, 0.6);
}

/* =========================================================
   PRODUCTS LIST TABLE VIEW
   ========================================================= */
.table-panel {
  background: var(--admin-card);
  border: 1px solid var(--border-panel);
  border-radius: 16px;
  padding: 24px;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
}

.table-toolbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 16px;
  margin-bottom: 20px;
  flex-wrap: wrap;
}

.table-search-field {
  background: var(--admin-input);
  border: 1px solid var(--border-panel);
  border-radius: 8px;
  padding: 8px 16px;
  color: #fff;
  font-size: 0.88rem;
  outline: none;
  min-width: 260px;
}

.custom-admin-table {
  width: 100%;
  border-collapse: collapse;
  text-align: left;
}

.custom-admin-table th {
  background: #11131B;
  color: var(--text-sub);
  font-size: 0.8rem;
  text-transform: uppercase;
  letter-spacing: 1px;
  padding: 14px 16px;
  border-bottom: 1px solid var(--border-panel);
}

.custom-admin-table td {
  padding: 14px 16px;
  border-bottom: 1px solid rgba(255, 255, 255, 0.05);
  font-size: 0.88rem;
  vertical-align: middle;
}

.custom-admin-table tr:hover td {
  background: var(--admin-card-hover);
}

.table-prod-img {
  width: 48px;
  height: 58px;
  object-fit: cover;
  border-radius: 6px;
  border: 1px solid var(--border-panel);
}

.badge-cat-men {
  background: rgba(59, 130, 246, 0.15);
  color: #60A5FA;
  padding: 3px 8px;
  border-radius: 4px;
  font-size: 0.75rem;
  font-weight: 600;
}
.badge-cat-women {
  background: rgba(236, 72, 153, 0.15);
  color: #F472B6;
  padding: 3px 8px;
  border-radius: 4px;
  font-size: 0.75rem;
  font-weight: 600;
}
.badge-cat-kids {
  background: rgba(16, 185, 129, 0.15);
  color: #34D399;
  padding: 3px 8px;
  border-radius: 4px;
  font-size: 0.75rem;
  font-weight: 600;
}

.stock-pill {
  display: inline-flex;
  align-items: center;
  gap: 6px;
  padding: 4px 10px;
  border-radius: 20px;
  font-size: 0.78rem;
  font-weight: 600;
}

.stock-pill.in-stock {
  background: rgba(16, 185, 129, 0.15);
  color: #34D399;
}
.stock-pill.low-stock {
  background: rgba(245, 158, 11, 0.15);
  color: #FBBF24;
}
.stock-pill.out-stock {
  background: rgba(239, 68, 68, 0.15);
  color: #F87171;
}

.table-action-btns {
  display: flex;
  gap: 8px;
}

.btn-table-action {
  background: var(--admin-input);
  border: 1px solid var(--border-panel);
  color: var(--text-main);
  width: 34px;
  height: 34px;
  border-radius: 6px;
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: all 0.2s;
}

.btn-table-action:hover {
  border-color: var(--admin-gold);
  color: var(--admin-gold-light);
}

.btn-table-action.delete:hover {
  border-color: #EF4444;
  color: #EF4444;
  background: rgba(239, 68, 68, 0.1);
}

/* =========================================================
   CUSTOMER ORDERS MANAGEMENT
   ========================================================= */
.order-status-select {
  background: var(--admin-input);
  border: 1px solid var(--border-panel);
  color: #fff;
  padding: 6px 10px;
  border-radius: 6px;
  font-size: 0.8rem;
  cursor: pointer;
  outline: none;
}

.order-status-badge {
  padding: 4px 10px;
  border-radius: 20px;
  font-size: 0.75rem;
  font-weight: 700;
  text-transform: uppercase;
}
.order-status-badge.Processing { background: rgba(59, 130, 246, 0.2); color: #60A5FA; }
.order-status-badge.Shipped { background: rgba(139, 92, 246, 0.2); color: #A78BFA; }
.order-status-badge.Delivered { background: rgba(16, 185, 129, 0.2); color: #34D399; }
.order-status-badge.Pending { background: rgba(245, 158, 11, 0.2); color: #FBBF24; }
.order-status-badge.Cancelled { background: rgba(239, 68, 68, 0.2); color: #F87171; }

/* Responsive */
@media (max-width: 1024px) {
  .admin-sidebar {
    width: 80px;
  }
  .sidebar-brand-name, .sidebar-brand-role, .sidebar-item-btn span, .store-live-btn span, .admin-logout-btn span {
    display: none;
  }
  .sidebar-item-btn {
    justify-content: center;
    padding: 14px;
  }
  .admin-metrics-grid {
    grid-template-columns: repeat(2, 1fr);
  }
  .add-product-grid {
    grid-template-columns: 1fr;
  }
}

@media (max-width: 768px) {
  .admin-layout {
    flex-direction: column;
  }
  .admin-sidebar {
    width: 100%;
    height: auto;
    position: relative;
  }
  .admin-main {
    padding: 20px 16px;
  }
  .admin-metrics-grid {
    grid-template-columns: 1fr;
  }
}
