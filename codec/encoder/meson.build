cpp_sources = [
  'core/src/au_set.cpp',
  'core/src/deblocking.cpp',
  'core/src/decode_mb_aux.cpp',
  'core/src/encode_mb_aux.cpp',
  'core/src/encoder.cpp',
  'core/src/encoder_data_tables.cpp',
  'core/src/encoder_ext.cpp',
  'core/src/get_intra_predictor.cpp',
  'core/src/md.cpp',
  'core/src/mv_pred.cpp',
  'core/src/nal_encap.cpp',
  'core/src/paraset_strategy.cpp',
  'core/src/picture_handle.cpp',
  'core/src/ratectl.cpp',
  'core/src/ref_list_mgr_svc.cpp',
  'core/src/sample.cpp',
  'core/src/set_mb_syn_cabac.cpp',
  'core/src/set_mb_syn_cavlc.cpp',
  'core/src/slice_multi_threading.cpp',
  'core/src/svc_base_layer_md.cpp',
  'core/src/svc_enc_slice_segment.cpp',
  'core/src/svc_encode_mb.cpp',
  'core/src/svc_encode_slice.cpp',
  'core/src/svc_mode_decision.cpp',
  'core/src/svc_motion_estimate.cpp',
  'core/src/svc_set_mb_syn_cabac.cpp',
  'core/src/svc_set_mb_syn_cavlc.cpp',
  'core/src/wels_preprocess.cpp',
  'core/src/wels_task_base.cpp',
  'core/src/wels_task_encoder.cpp',
  'core/src/wels_task_management.cpp',
  'plus/src/welsEncoderExt.cpp',
]

asm_sources = [
  'core/x86/coeff.asm',
  'core/x86/dct.asm',
  'core/x86/intra_pred.asm',
  'core/x86/matrix_transpose.asm',
  'core/x86/memzero.asm',
  'core/x86/quant.asm',
  'core/x86/sample_sc.asm',
  'core/x86/score.asm',
]

objs_asm = asm_gen.process(asm_sources)

libencoder = static_library('encoder', cpp_sources, objs_asm,
  include_directories: [inc, processing_inc, encoder_inc],
  dependencies: deps)
