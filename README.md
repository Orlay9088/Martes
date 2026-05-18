
<style>
*{box-sizing:border-box;margin:0;padding:0;font-family:var(--font-sans,sans-serif)}
:root{
  --cr:#C0392B;--cr-d:#922B21;--cr-dd:#6B1E17;
  --cr-l:#FADBD8;--cr-ll:#FEF0EE;
  --cy:#E8A020;--cy-d:#B07218;--cy-l:#FEF3DC;--cy-ll:#FFFBF0;
}

.app{border-radius:16px;overflow:hidden;border:0.5px solid var(--color-border-tertiary);background:var(--color-background-primary)}

.header{background:var(--cr);padding:18px 22px;display:flex;align-items:center;gap:14px}
.logo{width:50px;height:50px;border-radius:50%;background:var(--cy);display:flex;align-items:center;justify-content:center;flex-shrink:0}
.logo i{font-size:24px;color:var(--cr-d)}
.htext h1{font-size:19px;font-weight:500;color:#fff;line-height:1.2}
.htext p{font-size:12px;color:rgba(255,255,255,0.75);margin-top:2px}
.hbadge{margin-left:auto;background:var(--cy);border-radius:20px;padding:4px 12px;font-size:12px;font-weight:500;color:var(--cr-d);white-space:nowrap;flex-shrink:0}

.nav{background:var(--cr-d);display:flex;overflow-x:auto;scrollbar-width:none}
.nav::-webkit-scrollbar{display:none}
.nav button{background:none;border:none;border-bottom:2px solid transparent;color:rgba(255,255,255,0.6);padding:10px 16px;font-size:12px;cursor:pointer;white-space:nowrap;display:flex;align-items:center;gap:5px;transition:all 0.15s}
.nav button.on{color:var(--cy);border-bottom-color:var(--cy)}
.nav button:hover:not(.on){color:#fff}
.nav button i{font-size:15px}

.body{padding:20px 22px}
.sec{display:none}.sec.on{display:block}

.sec-label{font-size:11px;font-weight:500;letter-spacing:0.6px;color:var(--cr);text-transform:uppercase;margin-bottom:14px;display:flex;align-items:center;gap:6px}
.sec-label::after{content:'';flex:1;height:0.5px;background:var(--cr-l)}

.card{background:var(--color-background-primary);border:0.5px solid var(--color-border-tertiary);border-radius:12px;padding:16px;margin-bottom:12px}

.stamp-area{background:var(--cr-ll);border-radius:12px;padding:18px;margin-bottom:14px;border:0.5px solid var(--cr-l)}
.stamp-row{display:flex;justify-content:center;gap:12px;margin:12px 0}
.stamp{width:54px;height:54px;border-radius:50%;border:2px dashed var(--cr-l);display:flex;align-items:center;justify-content:center;cursor:pointer;transition:all 0.2s;background:var(--color-background-primary)}
.stamp i{font-size:22px;color:var(--cr-l)}
.stamp.on{background:var(--cy);border:2px solid var(--cy-d)}
.stamp.on i{color:var(--cr-d)}
.stamp-info{text-align:center;font-size:13px;color:var(--cr-d);font-weight:500}
.stamp-sub{text-align:center;font-size:11px;color:var(--cr);margin-top:3px}

.pbar{height:5px;background:var(--cr-l);border-radius:3px;margin:10px 0;overflow:hidden}
.pfill{height:100%;background:var(--cy);border-radius:3px;transition:width 0.4s}

.prize-box{background:var(--cy-l);border:1px solid var(--cy-d);border-radius:10px;padding:12px 14px;display:flex;align-items:flex-start;gap:10px;margin-top:10px}
.prize-box i{color:var(--cy-d);font-size:20px;flex-shrink:0;margin-top:1px}
.prize-box-body p{font-size:13px;font-weight:500;color:var(--cy-d)}
.prize-box-body span{font-size:11px;color:var(--cy-d);opacity:0.8}

.btn-row{display:flex;gap:8px;margin-top:12px}
.btn-main{background:var(--cr);color:#fff;border:none;border-radius:8px;padding:10px 0;font-size:13px;cursor:pointer;flex:1;display:flex;align-items:center;justify-content:center;gap:6px;transition:background 0.15s}
.btn-main:hover{background:var(--cr-d)}
.btn-main i{font-size:15px}
.btn-sec{background:transparent;color:var(--cr);border:1px solid var(--cr-l);border-radius:8px;padding:10px 16px;font-size:13px;cursor:pointer;transition:all 0.15s;white-space:nowrap}
.btn-sec:hover{background:var(--cr-ll)}

.reward-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:8px;margin-top:4px}
.reward-item{background:var(--cr-ll);border-radius:8px;padding:10px 8px;text-align:center;border:0.5px solid var(--cr-l)}
.reward-item i{font-size:20px;color:var(--cr);display:block;margin-bottom:4px}
.reward-item p{font-size:11px;color:var(--cr-d);line-height:1.3}

.combo-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(150px,1fr));gap:10px;margin-bottom:14px}
.combo{border-radius:12px;padding:16px;text-align:center;background:var(--color-background-primary);border:0.5px solid var(--color-border-tertiary);position:relative;overflow:hidden}
.combo::before{content:'';position:absolute;top:0;left:0;right:0;height:3px;background:var(--cr)}
.combo-emoji{font-size:28px;margin-bottom:6px;display:block}
.combo-name{font-size:13px;font-weight:500;color:var(--color-text-primary);margin-bottom:3px}
.combo-items{font-size:11px;color:var(--color-text-secondary);margin-bottom:8px;line-height:1.4}
.combo-price{font-size:20px;font-weight:500;color:var(--cr)}
.combo-btn{margin-top:10px;width:100%;background:var(--cr-ll);color:var(--cr-d);border:none;border-radius:6px;padding:7px 0;font-size:12px;cursor:pointer;font-weight:500;transition:background 0.15s}
.combo-btn:hover{background:var(--cr-l)}
.combo-tag{position:absolute;top:8px;right:8px;background:var(--cy);color:var(--cr-d);font-size:10px;padding:2px 6px;border-radius:4px;font-weight:500}

.kpi-g{display:grid;grid-template-columns:repeat(auto-fit,minmax(140px,1fr));gap:8px;margin-bottom:14px}
.kpi{background:var(--color-background-secondary);border-radius:10px;padding:14px 12px}
.kpi-label{font-size:10px;color:var(--color-text-secondary);text-transform:uppercase;letter-spacing:0.5px;margin-bottom:6px}
.kpi-val{font-size:22px;font-weight:500;color:var(--cr)}
.kpi-meta{font-size:11px;color:var(--color-text-secondary);margin-top:2px}
.kpi-bar{height:3px;background:var(--color-border-tertiary);border-radius:2px;margin-top:10px;overflow:hidden}
.kpi-fill{height:100%;background:var(--cy);border-radius:2px}

.insight-card{background:var(--cr-ll);border-radius:10px;padding:14px;border:0.5px solid var(--cr-l);margin-bottom:12px}
.insight-card h3{font-size:13px;font-weight:500;color:var(--cr-d);margin-bottom:8px;display:flex;align-items:center;gap:6px}
.insight-card h3 i{font-size:15px}
.insight-list{display:flex;flex-direction:column;gap:6px}
.insight-row{display:flex;align-items:center;gap:8px;font-size:12px;color:var(--cr-d)}
.insight-row i{font-size:14px;flex-shrink:0}

.tl{display:flex;flex-direction:column;gap:0}
.tl-item{display:flex;gap:14px;padding-bottom:20px;position:relative}
.tl-item:not(:last-child)::after{content:'';position:absolute;left:15px;top:32px;bottom:0;width:1px;background:var(--color-border-tertiary)}
.tl-dot{width:32px;height:32px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:14px;flex-shrink:0;z-index:1}
.tl-dot.done{background:var(--cy);color:var(--cr-d)}
.tl-dot.prog{background:var(--cr);color:#fff}
.tl-dot.next{background:var(--color-background-secondary);color:var(--color-text-secondary);border:0.5px solid var(--color-border-tertiary)}
.tl-body{padding-top:5px;flex:1}
.tl-title{font-size:13px;font-weight:500;color:var(--color-text-primary)}
.tl-time{font-size:11px;color:var(--color-text-secondary);margin-top:2px}
.tl-chip{display:inline-block;font-size:10px;padding:2px 8px;border-radius:4px;margin-top:5px;font-weight:500}
.tl-chip.done{background:var(--cy-l);color:var(--cy-d)}
.tl-chip.prog{background:var(--cr-l);color:var(--cr-d)}
.tl-chip.next{background:var(--color-background-secondary);color:var(--color-text-secondary)}

.canal-list{display:flex;flex-direction:column;gap:10px;margin-bottom:14px}
.canal{display:flex;align-items:center;gap:12px;background:var(--color-background-secondary);border-radius:10px;padding:12px 14px}
.canal-ico{width:40px;height:40px;border-radius:8px;display:flex;align-items:center;justify-content:center;font-size:20px;flex-shrink:0}
.canal-ico.wa{background:#E6F7EF;color:#25D366}
.canal-ico.ig{background:#FDE8EE;color:#E1306C}
.canal-ico.fb{background:#E8EEFF;color:#1877F2}
.canal-body{flex:1}
.canal-name{font-size:13px;font-weight:500;color:var(--color-text-primary)}
.canal-desc{font-size:11px;color:var(--color-text-secondary);margin-top:2px}
.canal-chip{font-size:10px;background:var(--cr-ll);color:var(--cr-d);border-radius:4px;padding:3px 8px;white-space:nowrap;font-weight:500}
.canal-chip.med{background:var(--color-background-secondary);color:var(--color-text-secondary)}

.content-grid{display:grid;grid-template-columns:1fr 1fr;gap:8px}
.content-item{background:var(--color-background-primary);border:0.5px solid var(--color-border-tertiary);border-radius:8px;padding:10px 12px;display:flex;align-items:flex-start;gap:8px}
.content-item i{color:var(--cr);font-size:16px;flex-shrink:0;margin-top:1px}
.content-item p{font-size:12px;color:var(--color-text-primary);line-height:1.4}

.toast{display:none;background:var(--cr-d);color:#fff;border-radius:20px;padding:9px 18px;font-size:12px;text-align:center;margin-top:12px}
.toast.show{display:block}
</style>

<h2 class="sr-only">App Claire Contigo — sistema de fidelización para Claire Repostería con tarjeta de sellos, combos, métricas, cronograma y canales digitales</h2>

<div class="app">

  <div class="header">
    <div class="logo"><i class="ti ti-cookie" aria-hidden="true"></i></div>
    <div class="htext">
      <h1>Claire Contigo</h1>
      <p>Tu programa de fidelización</p>
    </div>
    <div class="hbadge"><i class="ti ti-map-pin" style="font-size:12px;vertical-align:-1px" aria-hidden="true"></i> Medellín</div>
  </div>

  <div class="nav">
    <button class="on" onclick="tab('inicio',this)"><i class="ti ti-home" aria-hidden="true"></i> Inicio</button>
    <button onclick="tab('tarjeta',this)"><i class="ti ti-star" aria-hidden="true"></i> Mi tarjeta</button>
    <button onclick="tab('combos',this)"><i class="ti ti-package" aria-hidden="true"></i> Combos</button>
    <button onclick="tab('metricas',this)"><i class="ti ti-chart-bar" aria-hidden="true"></i> Métricas</button>
    <button onclick="tab('plan',this)"><i class="ti ti-calendar" aria-hidden="true"></i> Plan</button>
    <button onclick="tab('canales',this)"><i class="ti ti-broadcast" aria-hidden="true"></i> Canales</button>
  </div>

  <div class="body">
    <div id="toast" class="toast"></div>

    <!-- INICIO -->
    <div id="inicio" class="sec on">
      <div class="sec-label"><i class="ti ti-sparkles" aria-hidden="true"></i> Bienvenida</div>

      <div class="card" style="display:flex;align-items:center;gap:14px;padding:18px">
        <div style="width:52px;height:52px;border-radius:50%;background:var(--cr);display:flex;align-items:center;justify-content:center;flex-shrink:0">
          <i class="ti ti-heart" style="font-size:24px;color:#fff" aria-hidden="true"></i>
        </div>
        <div>
          <p style="font-size:15px;font-weight:500;color:var(--color-text-primary)">Estrategia "Claire Contigo"</p>
          <p style="font-size:12px;color:var(--color-text-secondary);margin-top:3px;line-height:1.5">Fidelización basada en cercanía, recompensas y comunicación constante con tus clientes del sector.</p>
        </div>
      </div>

      <div style="display:grid;grid-template-columns:1fr 1fr;gap:8px;margin-bottom:12px">
        <div style="background:var(--cr-ll);border-radius:10px;padding:14px;border:0.5px solid var(--cr-l);text-align:center;cursor:pointer" onclick="tab('tarjeta',document.querySelectorAll('.nav button')[1])">
          <i class="ti ti-star" style="font-size:24px;color:var(--cr);display:block;margin-bottom:6px" aria-hidden="true"></i>
          <p style="font-size:13px;font-weight:500;color:var(--cr-d)">Mi tarjeta</p>
          <p style="font-size:11px;color:var(--cr);margin-top:2px">Acumula sellos</p>
        </div>
        <div style="background:var(--cy-l);border-radius:10px;padding:14px;border:0.5px solid var(--cy-d);text-align:center;cursor:pointer" onclick="tab('combos',document.querySelectorAll('.nav button')[2])">
          <i class="ti ti-package" style="font-size:24px;color:var(--cy-d);display:block;margin-bottom:6px" aria-hidden="true"></i>
          <p style="font-size:13px;font-weight:500;color:var(--cy-d)">Combos del día</p>
          <p style="font-size:11px;color:var(--cy-d);opacity:0.8;margin-top:2px">Desde $8.500</p>
        </div>
        <div style="background:var(--color-background-secondary);border-radius:10px;padding:14px;text-align:center;cursor:pointer" onclick="tab('metricas',document.querySelectorAll('.nav button')[3])">
          <i class="ti ti-chart-line" style="font-size:24px;color:var(--color-text-secondary);display:block;margin-bottom:6px" aria-hidden="true"></i>
          <p style="font-size:13px;font-weight:500;color:var(--color-text-primary)">Métricas</p>
          <p style="font-size:11px;color:var(--color-text-secondary);margin-top:2px">Ver indicadores</p>
        </div>
        <div style="background:var(--color-background-secondary);border-radius:10px;padding:14px;text-align:center;cursor:pointer" onclick="tab('canales',document.querySelectorAll('.nav button')[5])">
          <i class="ti ti-brand-whatsapp" style="font-size:24px;color:var(--color-text-secondary);display:block;margin-bottom:6px" aria-hidden="true"></i>
          <p style="font-size:13px;font-weight:500;color:var(--color-text-primary)">Canales</p>
          <p style="font-size:11px;color:var(--color-text-secondary);margin-top:2px">WA · Instagram · FB</p>
        </div>
      </div>

      <div class="insight-card">
        <h3><i class="ti ti-bulb" aria-hidden="true"></i> Diagnóstico del negocio</h3>
        <div style="display:grid;grid-template-columns:1fr 1fr;gap:8px">
          <div>
            <p style="font-size:10px;font-weight:500;color:var(--cr-d);text-transform:uppercase;letter-spacing:0.4px;margin-bottom:6px">Fortalezas</p>
            <div class="insight-list">
              <div class="insight-row"><i class="ti ti-check" aria-hidden="true"></i> Atención cercana</div>
              <div class="insight-row"><i class="ti ti-check" aria-hidden="true"></i> Productos variados</div>
              <div class="insight-row"><i class="ti ti-check" aria-hidden="true"></i> Precios accesibles</div>
              <div class="insight-row"><i class="ti ti-check" aria-hidden="true"></i> Entrega rápida</div>
            </div>
          </div>
          <div>
            <p style="font-size:10px;font-weight:500;color:var(--cr-d);text-transform:uppercase;letter-spacing:0.4px;margin-bottom:6px">A mejorar</p>
            <div class="insight-list">
              <div class="insight-row"><i class="ti ti-arrow-up" aria-hidden="true"></i> Visibilidad menú</div>
              <div class="insight-row"><i class="ti ti-arrow-up" aria-hidden="true"></i> Identidad visual</div>
              <div class="insight-row"><i class="ti ti-arrow-up" aria-hidden="true"></i> Presencia digital</div>
              <div class="insight-row"><i class="ti ti-arrow-up" aria-hidden="true"></i> Retención clientes</div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- TARJETA -->
    <div id="tarjeta" class="sec">
      <div class="sec-label"><i class="ti ti-star" aria-hidden="true"></i> Tarjeta cliente frecuente</div>

      <div class="stamp-area">
        <p style="font-size:11px;font-weight:500;color:var(--cr-d);text-align:center;text-transform:uppercase;letter-spacing:0.5px">Compras registradas</p>
        <div class="stamp-row" id="stamps"></div>
        <div class="pbar"><div class="pfill" id="pfill" style="width:0%"></div></div>
        <p class="stamp-info" id="sinfo">0 / 5 sellos</p>
        <p class="stamp-sub" id="ssub">Cada compra mayor a $15.000 suma un sello</p>
        <div id="prize" style="display:none">
          <div class="prize-box" style="margin-top:12px">
            <i class="ti ti-gift" aria-hidden="true"></i>
            <div class="prize-box-body">
              <p>¡Tarjeta completa! Elige tu premio</p>
              <span>Bebida gratis · 15% descuento · Producto cortesía</span>
            </div>
          </div>
        </div>
        <div class="btn-row">
          <button class="btn-main" onclick="addStamp()"><i class="ti ti-plus" aria-hidden="true"></i> Registrar compra</button>
          <button class="btn-sec" onclick="resetS()"><i class="ti ti-refresh" aria-hidden="true"></i></button>
        </div>
      </div>

      <div class="sec-label"><i class="ti ti-gift" aria-hidden="true"></i> Premios disponibles</div>
      <div class="reward-grid">
        <div class="reward-item">
          <i class="ti ti-cup" aria-hidden="true"></i>
          <p>Bebida gratis de tu elección</p>
        </div>
        <div class="reward-item">
          <i class="ti ti-discount-2" aria-hidden="true"></i>
          <p>15% descuento próxima compra</p>
        </div>
        <div class="reward-item">
          <i class="ti ti-cookie" aria-hidden="true"></i>
          <p>Producto pequeño de cortesía</p>
        </div>
      </div>

      <div class="card" style="margin-top:12px;display:flex;align-items:center;gap:10px">
        <i class="ti ti-info-circle" style="color:var(--cr);font-size:18px;flex-shrink:0" aria-hidden="true"></i>
        <p style="font-size:12px;color:var(--color-text-secondary);line-height:1.5">El objetivo es lograr <strong style="color:var(--cr-d);font-weight:500">100 clientes fidelizados</strong> en los primeros 3 meses e incrementar la recompra un 25%.</p>
      </div>
    </div>

    <!-- COMBOS -->
    <div id="combos" class="sec">
      <div class="sec-label"><i class="ti ti-package" aria-hidden="true"></i> Combos promocionales</div>
      <div class="combo-grid">
        <div class="combo">
          <span class="combo-tag">Popular</span>
          <span class="combo-emoji">☕</span>
          <p class="combo-name">Combo Café</p>
          <p class="combo-items">Café + pastel pequeño</p>
          <p class="combo-price">$15.500</p>
          <button class="combo-btn" onclick="toast('¡Combo Café agregado!')">Pedir</button>
        </div>
        <div class="combo">
          <span class="combo-emoji">🥐</span>
          <p class="combo-name">Combo Tradicional</p>
          <p class="combo-items">Gaseosa + panadería selección</p>
          <p class="combo-price">$18.000</p>
          <button class="combo-btn" onclick="toast('¡Combo Tradicional agregado!')">Pedir</button>
        </div>
        <div class="combo">
          <span class="combo-emoji">🍮</span>
          <p class="combo-name">Tarde Dulce</p>
          <p class="combo-items">Postre + bebida a elegir</p>
          <p class="combo-price">$22.000</p>
          <button class="combo-btn" onclick="toast('¡Tarde Dulce agregado!')">Pedir</button>
        </div>
      </div>

      <div class="insight-card">
        <h3><i class="ti ti-trending-up" aria-hidden="true"></i> Impacto esperado de los combos</h3>
        <div class="insight-list">
          <div class="insight-row"><i class="ti ti-check" aria-hidden="true"></i> Mayor rotación de productos del inventario</div>
          <div class="insight-row"><i class="ti ti-check" aria-hidden="true"></i> Ticket promedio incrementado un 10%</div>
          <div class="insight-row"><i class="ti ti-check" aria-hidden="true"></i> Mejor percepción de precio en clientes de paso</div>
          <div class="insight-row"><i class="ti ti-check" aria-hidden="true"></i> 30% de clientes participando en promociones</div>
        </div>
      </div>
    </div>

    <!-- MÉTRICAS -->
    <div id="metricas" class="sec">
      <div class="sec-label"><i class="ti ti-chart-bar" aria-hidden="true"></i> Indicadores de gestión</div>
      <div class="kpi-g">
        <div class="kpi">
          <div class="kpi-label">Recompra</div>
          <div class="kpi-val">+25%</div>
          <div class="kpi-meta">Meta frecuencia</div>
          <div class="kpi-bar"><div class="kpi-fill" style="width:38%"></div></div>
        </div>
        <div class="kpi">
          <div class="kpi-label">Clientes fidelizados</div>
          <div class="kpi-val">100</div>
          <div class="kpi-meta">En 3 meses</div>
          <div class="kpi-bar"><div class="kpi-fill" style="width:22%"></div></div>
        </div>
        <div class="kpi">
          <div class="kpi-label">Ventas totales</div>
          <div class="kpi-val">+15%</div>
          <div class="kpi-meta">Incremento mensual</div>
          <div class="kpi-bar"><div class="kpi-fill" style="width:30%"></div></div>
        </div>
        <div class="kpi">
          <div class="kpi-label">Alcance digital</div>
          <div class="kpi-val">+40%</div>
          <div class="kpi-meta">Redes sociales</div>
          <div class="kpi-bar"><div class="kpi-fill" style="width:14%"></div></div>
        </div>
        <div class="kpi">
          <div class="kpi-label">Ticket promedio</div>
          <div class="kpi-val">+10%</div>
          <div class="kpi-meta">Valor por compra</div>
          <div class="kpi-bar"><div class="kpi-fill" style="width:25%"></div></div>
        </div>
        <div class="kpi">
          <div class="kpi-label">Uso de promo</div>
          <div class="kpi-val">30%</div>
          <div class="kpi-meta">Clientes activos</div>
          <div class="kpi-bar"><div class="kpi-fill" style="width:18%"></div></div>
        </div>
      </div>

      <div class="card">
        <p style="font-size:13px;font-weight:500;color:var(--color-text-primary);margin-bottom:10px;display:flex;align-items:center;gap:6px"><i class="ti ti-eye" style="color:var(--cr);font-size:16px" aria-hidden="true"></i> Resultados esperados al mes 3</p>
        <div style="display:flex;flex-direction:column;gap:8px">
          <div style="display:flex;align-items:center;justify-content:space-between;font-size:12px">
            <span style="color:var(--color-text-secondary)">Flujo de clientes</span>
            <span style="color:var(--cr-d);font-weight:500">Mayor tráfico semanal</span>
          </div>
          <div style="display:flex;align-items:center;justify-content:space-between;font-size:12px">
            <span style="color:var(--color-text-secondary)">Posicionamiento local</span>
            <span style="color:var(--cr-d);font-weight:500">Reconocimiento sector</span>
          </div>
          <div style="display:flex;align-items:center;justify-content:space-between;font-size:12px">
            <span style="color:var(--color-text-secondary)">Experiencia de compra</span>
            <span style="color:var(--cr-d);font-weight:500">Más organizada y visual</span>
          </div>
        </div>
      </div>
    </div>

    <!-- PLAN -->
    <div id="plan" class="sec">
      <div class="sec-label"><i class="ti ti-calendar" aria-hidden="true"></i> Cronograma de implementación</div>
      <div class="tl">
        <div class="tl-item">
          <div class="tl-dot done"><i class="ti ti-check" aria-hidden="true"></i></div>
          <div class="tl-body">
            <div class="tl-title">Diseño de la estrategia</div>
            <div class="tl-time">Semana 1</div>
            <span class="tl-chip done">Completado</span>
          </div>
        </div>
        <div class="tl-item">
          <div class="tl-dot prog"><i class="ti ti-id-badge" aria-hidden="true"></i></div>
          <div class="tl-body">
            <div class="tl-title">Creación de tarjetas de cliente</div>
            <div class="tl-time">Semanas 1 – 2</div>
            <span class="tl-chip prog">En progreso</span>
          </div>
        </div>
        <div class="tl-item">
          <div class="tl-dot prog"><i class="ti ti-discount" aria-hidden="true"></i></div>
          <div class="tl-body">
            <div class="tl-title">Diseño de combos y promociones</div>
            <div class="tl-time">Semanas 2 – 3</div>
            <span class="tl-chip prog">En progreso</span>
          </div>
        </div>
        <div class="tl-item">
          <div class="tl-dot next"><i class="ti ti-brand-instagram" aria-hidden="true"></i></div>
          <div class="tl-body">
            <div class="tl-title">Redes sociales y plan de contenido</div>
            <div class="tl-time">Semanas 2 – 4</div>
            <span class="tl-chip next">Próximo</span>
          </div>
        </div>
        <div class="tl-item">
          <div class="tl-dot next"><i class="ti ti-brand-whatsapp" aria-hidden="true"></i></div>
          <div class="tl-body">
            <div class="tl-title">WhatsApp Business activo</div>
            <div class="tl-time">Semanas 3 – 4</div>
            <span class="tl-chip next">Próximo</span>
          </div>
        </div>
        <div class="tl-item">
          <div class="tl-dot next"><i class="ti ti-rocket" aria-hidden="true"></i></div>
          <div class="tl-body">
            <div class="tl-title">Lanzamiento oficial "Claire Contigo"</div>
            <div class="tl-time">Semana 4</div>
            <span class="tl-chip next">Próximo</span>
          </div>
        </div>
        <div class="tl-item">
          <div class="tl-dot next"><i class="ti ti-chart-line" aria-hidden="true"></i></div>
          <div class="tl-body">
            <div class="tl-title">Seguimiento de KPIs y evaluación</div>
            <div class="tl-time">Mes 2 – Mes 3</div>
            <span class="tl-chip next">Próximo</span>
          </div>
        </div>
      </div>

      <div class="card" style="display:flex;gap:10px;align-items:flex-start">
        <i class="ti ti-coins" style="color:var(--cy-d);font-size:20px;flex-shrink:0;margin-top:1px" aria-hidden="true"></i>
        <div>
          <p style="font-size:13px;font-weight:500;color:var(--color-text-primary);margin-bottom:3px">Recursos necesarios</p>
          <p style="font-size:12px;color:var(--color-text-secondary);line-height:1.5">La estrategia no requiere grandes inversiones. Equipo del local + responsable de redes + impresión de tarjetas + piezas visuales básicas.</p>
        </div>
      </div>
    </div>

    <!-- CANALES -->
    <div id="canales" class="sec">
      <div class="sec-label"><i class="ti ti-broadcast" aria-hidden="true"></i> Canales digitales</div>
      <div class="canal-list">
        <div class="canal">
          <div class="canal-ico wa"><i class="ti ti-brand-whatsapp" aria-hidden="true"></i></div>
          <div class="canal-body">
            <div class="canal-name">WhatsApp Business</div>
            <div class="canal-desc">Promociones semanales · Nuevos productos · Fechas especiales · Base de datos de clientes</div>
          </div>
          <span class="canal-chip">Prioridad alta</span>
        </div>
        <div class="canal">
          <div class="canal-ico ig"><i class="ti ti-brand-instagram" aria-hidden="true"></i></div>
          <div class="canal-body">
            <div class="canal-name">Instagram</div>
            <div class="canal-desc">Fotos de tortas · Historias artesanales · Combos del día · Interacción con clientes</div>
          </div>
          <span class="canal-chip">Prioridad alta</span>
        </div>
        <div class="canal">
          <div class="canal-ico fb"><i class="ti ti-brand-facebook" aria-hidden="true"></i></div>
          <div class="canal-body">
            <div class="canal-name">Facebook</div>
            <div class="canal-desc">Promociones · Productos destacados · Alcance local del sector</div>
          </div>
          <span class="canal-chip med">Media</span>
        </div>
      </div>

      <div class="sec-label"><i class="ti ti-camera" aria-hidden="true"></i> Ideas de contenido semanal</div>
      <div class="content-grid">
        <div class="content-item">
          <i class="ti ti-camera" aria-hidden="true"></i>
          <p>Foto del producto estrella del día</p>
        </div>
        <div class="content-item">
          <i class="ti ti-video" aria-hidden="true"></i>
          <p>Historia del proceso artesanal</p>
        </div>
        <div class="content-item">
          <i class="ti ti-discount-2" aria-hidden="true"></i>
          <p>Anuncio del combo de la semana</p>
        </div>
        <div class="content-item">
          <i class="ti ti-message-circle" aria-hidden="true"></i>
          <p>Testimonio de cliente satisfecho</p>
        </div>
        <div class="content-item">
          <i class="ti ti-calendar-event" aria-hidden="true"></i>
          <p>Recordatorio de fechas especiales</p>
        </div>
        <div class="content-item">
          <i class="ti ti-clock" aria-hidden="true"></i>
          <p>Horarios y novedades del local</p>
        </div>
      </div>
    </div>

  </div>
</div>

<script>
let n=0;
function renderStamps(){
  const g=document.getElementById('stamps');
  if(!g)return;
  g.innerHTML='';
  for(let i=0;i<5;i++){
    const d=document.createElement('div');
    d.className='stamp'+(i<n?' on':'');
    const ic=document.createElement('i');
    ic.className=i<n?'ti ti-star':'ti ti-circle';
    ic.setAttribute('aria-hidden','true');
    d.appendChild(ic);
    g.appendChild(d);
  }
  const pct=Math.round((n/5)*100);
  document.getElementById('pfill').style.width=pct+'%';
  document.getElementById('sinfo').textContent=n+' / 5 sellos';
  document.getElementById('ssub').textContent=n>=5?'¡Reclama tu premio en caja!':'Faltan '+(5-n)+' para tu próximo premio';
  const pr=document.getElementById('prize');
  if(pr)pr.style.display=n>=5?'block':'none';
}
function addStamp(){
  if(n<5){n++;renderStamps();toast(n<5?'¡Sello registrado! '+n+'/5':'🎉 ¡Premio desbloqueado! Habla con el equipo');}
  else toast('Tarjeta completa — reclama tu premio primero');
}
function resetS(){n=0;renderStamps();toast('Tarjeta reiniciada');}
function toast(msg){
  const t=document.getElementById('toast');
  if(!t)return;
  t.textContent=msg;t.classList.add('show');
  setTimeout(()=>t.classList.remove('show'),2500);
}
function tab(id,btn){
  document.querySelectorAll('.sec').forEach(s=>s.classList.remove('on'));
  document.querySelectorAll('.nav button').forEach(b=>b.classList.remove('on'));
  const s=document.getElementById(id);
  if(s)s.classList.add('on');
  if(btn)btn.classList.add('on');
}
renderStamps();
</script>
