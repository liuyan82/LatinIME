

cmake_minimum_required(VERSION 3.6)

include_directories(
        src
        src/utils
        )

add_library("jni_latinime"
       SHARED
        com_android_inputmethod_keyboard_ProximityInfo.cpp
        com_android_inputmethod_latin_BinaryDictionary.cpp
        com_android_inputmethod_latin_BinaryDictionaryUtils.cpp
        com_android_inputmethod_latin_DicTraverseSession.cpp
        jni_common.cpp
        src/dictionary/header/header_policy.cpp
        src/dictionary/header/header_read_write_utils.cpp
        src/dictionary/property/ngram_context.cpp
        src/dictionary/structure/dictionary_structure_with_buffer_policy_factory.cpp
        src/dictionary/structure/pt_common/bigram/bigram_list_read_write_utils.cpp
        src/dictionary/structure/pt_common/dynamic_pt_gc_event_listeners.cpp
        src/dictionary/structure/pt_common/dynamic_pt_reading_helper.cpp
        src/dictionary/structure/pt_common/dynamic_pt_reading_utils.cpp
        src/dictionary/structure/pt_common/dynamic_pt_updating_helper.cpp
        src/dictionary/structure/pt_common/dynamic_pt_writing_utils.cpp
        src/dictionary/structure/pt_common/patricia_trie_reading_utils.cpp
        src/dictionary/structure/pt_common/shortcut/shortcut_list_reading_utils.cpp
        src/dictionary/structure/v2/patricia_trie_policy.cpp
        src/dictionary/structure/v2/ver2_patricia_trie_node_reader.cpp
        src/dictionary/structure/v2/ver2_pt_node_array_reader.cpp
        src/dictionary/structure/v4/ver4_dict_buffers.cpp
        src/dictionary/structure/v4/ver4_dict_constants.cpp
        src/dictionary/structure/v4/ver4_patricia_trie_node_reader.cpp
        src/dictionary/structure/v4/ver4_patricia_trie_node_writer.cpp
        src/dictionary/structure/v4/ver4_patricia_trie_policy.cpp
        src/dictionary/structure/v4/ver4_patricia_trie_reading_utils.cpp
        src/dictionary/structure/v4/ver4_patricia_trie_writing_helper.cpp
        src/dictionary/structure/v4/ver4_pt_node_array_reader.cpp
        src/dictionary/structure/v4/content/dynamic_language_model_probability_utils.cpp
        src/dictionary/structure/v4/content/language_model_dict_content.cpp
        src/dictionary/structure/v4/content/language_model_dict_content_global_counters.cpp
        src/dictionary/structure/v4/content/shortcut_dict_content.cpp
        src/dictionary/structure/v4/content/sparse_table_dict_content.cpp
        src/dictionary/structure/v4/content/terminal_position_lookup_table.cpp
        src/dictionary/utils/buffer_with_extendable_buffer.cpp
        src/dictionary/utils/byte_array_utils.cpp
        src/dictionary/utils/dict_file_writing_utils.cpp
        src/dictionary/utils/file_utils.cpp
        src/dictionary/utils/forgetting_curve_utils.cpp
        src/dictionary/utils/format_utils.cpp
        src/dictionary/utils/mmapped_buffer.cpp
        src/dictionary/utils/multi_bigram_map.cpp
        src/dictionary/utils/probability_utils.cpp
        src/dictionary/utils/sparse_table.cpp
        src/dictionary/utils/trie_map.cpp
        src/suggest/core/suggest.cpp
        src/suggest/core/dicnode/dic_node.cpp
        src/suggest/core/dicnode/dic_node_utils.cpp
        src/suggest/core/dicnode/dic_nodes_cache.cpp
        src/suggest/core/dictionary/dictionary.cpp
        src/suggest/core/dictionary/dictionary_utils.cpp
        src/suggest/core/dictionary/digraph_utils.cpp
        src/suggest/core/dictionary/error_type_utils.cpp
        src/suggest/core/layout/additional_proximity_chars.cpp
        src/suggest/core/layout/proximity_info.cpp
        src/suggest/core/layout/proximity_info_params.cpp
        src/suggest/core/layout/proximity_info_state.cpp
        src/suggest/core/layout/proximity_info_state_utils.cpp
        src/suggest/core/policy/weighting.cpp
        src/suggest/core/session/dic_traverse_session.cpp
        src/suggest/core/result/suggestion_results.cpp
        src/suggest/core/result/suggestions_output_utils.cpp
        src/suggest/policyimpl/gesture/gesture_suggest_policy_factory.cpp
        src/suggest/policyimpl/typing/scoring_params.cpp
        src/suggest/policyimpl/typing/typing_scoring.cpp
        src/suggest/policyimpl/typing/typing_suggest_policy.cpp
        src/suggest/policyimpl/typing/typing_traversal.cpp
        src/suggest/policyimpl/typing/typing_weighting.cpp
        src/utils/autocorrection_threshold_utils.cpp
        src/utils/char_utils.cpp
        src/utils/jni_data_utils.cpp
        src/utils/log_utils.cpp
        src/utils/time_keeper.cpp

        src/dictionary/structure/backward/v402/ver4_dict_buffers.cpp
        src/dictionary/structure/backward/v402/ver4_dict_constants.cpp
        src/dictionary/structure/backward/v402/ver4_patricia_trie_node_reader.cpp
        src/dictionary/structure/backward/v402/ver4_patricia_trie_node_writer.cpp
        src/dictionary/structure/backward/v402/ver4_patricia_trie_policy.cpp
        src/dictionary/structure/backward/v402/ver4_patricia_trie_reading_utils.cpp
        src/dictionary/structure/backward/v402/ver4_patricia_trie_writing_helper.cpp
        src/dictionary/structure/backward/v402/ver4_pt_node_array_reader.cpp
        src/dictionary/structure/backward/v402/content/bigram_dict_content.cpp
        src/dictionary/structure/backward/v402/content/probability_dict_content.cpp
        src/dictionary/structure/backward/v402/content/shortcut_dict_content.cpp
        src/dictionary/structure/backward/v402/content/sparse_table_dict_content.cpp
        src/dictionary/structure/backward/v402/content/terminal_position_lookup_table.cpp
        src/dictionary/structure/backward/v402/bigram/ver4_bigram_list_policy.cpp
        )