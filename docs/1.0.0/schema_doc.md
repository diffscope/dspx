# DiffScope Project Exchange Format

- [1. Property `DiffScope Project Exchange Format > content`](#content)
  - [1.1. Property `DiffScope Project Exchange Format > content > global`](#content_global)
    - [1.1.1. Property `DiffScope Project Exchange Format > content > global > author`](#content_global_author)
    - [1.1.2. Property `DiffScope Project Exchange Format > content > global > centShift`](#content_global_centShift)
    - [1.1.3. Property `DiffScope Project Exchange Format > content > global > editorId`](#content_global_editorId)
    - [1.1.4. Property `DiffScope Project Exchange Format > content > global > editorName`](#content_global_editorName)
    - [1.1.5. Property `DiffScope Project Exchange Format > content > global > name`](#content_global_name)
  - [1.2. Property `DiffScope Project Exchange Format > content > master`](#content_master)
    - [1.2.1. Property `DiffScope Project Exchange Format > content > master > control`](#content_master_control)
      - [1.2.1.1. Property `DiffScope Project Exchange Format > content > master > control > gain`](#content_master_control_gain)
      - [1.2.1.2. Property `DiffScope Project Exchange Format > content > master > control > mute`](#content_master_control_mute)
      - [1.2.1.3. Property `DiffScope Project Exchange Format > content > master > control > pan`](#content_master_control_pan)
  - [1.3. Property `DiffScope Project Exchange Format > content > timeline`](#content_timeline)
    - [1.3.1. Property `DiffScope Project Exchange Format > content > timeline > labels`](#content_timeline_labels)
      - [1.3.1.1. DiffScope Project Exchange Format > content > timeline > labels > Label](#content_timeline_labels_items)
        - [1.3.1.1.1. Property `DiffScope Project Exchange Format > content > timeline > labels > Label > pos`](#content_timeline_labels_items_pos)
        - [1.3.1.1.2. Property `DiffScope Project Exchange Format > content > timeline > labels > Label > text`](#content_timeline_labels_items_text)
    - [1.3.2. Property `DiffScope Project Exchange Format > content > timeline > tempos`](#content_timeline_tempos)
      - [1.3.2.1. DiffScope Project Exchange Format > content > timeline > tempos > Tempo](#content_timeline_tempos_items)
        - [1.3.2.1.1. Property `DiffScope Project Exchange Format > content > timeline > tempos > Tempo > pos`](#content_timeline_tempos_items_pos)
        - [1.3.2.1.2. Property `DiffScope Project Exchange Format > content > timeline > tempos > Tempo > value`](#content_timeline_tempos_items_value)
    - [1.3.3. Property `DiffScope Project Exchange Format > content > timeline > timeSignatures`](#content_timeline_timeSignatures)
      - [1.3.3.1. DiffScope Project Exchange Format > content > timeline > timeSignatures > Time Signature](#content_timeline_timeSignatures_items)
        - [1.3.3.1.1. Property `DiffScope Project Exchange Format > content > timeline > timeSignatures > Time Signature > denominator`](#content_timeline_timeSignatures_items_denominator)
        - [1.3.3.1.2. Property `DiffScope Project Exchange Format > content > timeline > timeSignatures > Time Signature > index`](#content_timeline_timeSignatures_items_index)
        - [1.3.3.1.3. Property `DiffScope Project Exchange Format > content > timeline > timeSignatures > Time Signature > numerator`](#content_timeline_timeSignatures_items_numerator)
  - [1.4. Property `DiffScope Project Exchange Format > content > tracks`](#content_tracks)
    - [1.4.1. DiffScope Project Exchange Format > content > tracks > Track](#content_tracks_items)
      - [1.4.1.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips`](#content_tracks_items_clips)
        - [1.4.1.1.1. DiffScope Project Exchange Format > content > tracks > Track > clips > Clip](#content_tracks_items_clips_items)
          - [1.4.1.1.1.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Audio Clip`](#content_tracks_items_clips_items_oneOf_i0)
            - [1.4.1.1.1.1.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Audio Clip > control`](#content_tracks_items_clips_items_oneOf_i0_control)
              - [1.4.1.1.1.1.1.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Audio Clip > control > gain`](#content_tracks_items_clips_items_oneOf_i0_control_gain)
              - [1.4.1.1.1.1.1.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Audio Clip > control > mute`](#content_tracks_items_clips_items_oneOf_i0_control_mute)
              - [1.4.1.1.1.1.1.3. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Audio Clip > control > pan`](#content_tracks_items_clips_items_oneOf_i0_control_pan)
            - [1.4.1.1.1.1.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Audio Clip > name`](#content_tracks_items_clips_items_oneOf_i0_name)
            - [1.4.1.1.1.1.3. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Audio Clip > path`](#content_tracks_items_clips_items_oneOf_i0_path)
            - [1.4.1.1.1.1.4. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Audio Clip > time`](#content_tracks_items_clips_items_oneOf_i0_time)
              - [1.4.1.1.1.1.4.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Audio Clip > time > clipLen`](#content_tracks_items_clips_items_oneOf_i0_time_clipLen)
              - [1.4.1.1.1.1.4.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Audio Clip > time > clipStart`](#content_tracks_items_clips_items_oneOf_i0_time_clipStart)
              - [1.4.1.1.1.1.4.3. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Audio Clip > time > length`](#content_tracks_items_clips_items_oneOf_i0_time_length)
              - [1.4.1.1.1.1.4.4. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Audio Clip > time > start`](#content_tracks_items_clips_items_oneOf_i0_time_start)
            - [1.4.1.1.1.1.5. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Audio Clip > type`](#content_tracks_items_clips_items_oneOf_i0_type)
            - [1.4.1.1.1.1.6. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Audio Clip > workspace`](#content_tracks_items_clips_items_oneOf_i0_workspace)
              - [1.4.1.1.1.1.6.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Audio Clip > workspace > Workspace Item`](#content_tracks_items_clips_items_oneOf_i0_workspace_additionalProperties)
          - [1.4.1.1.1.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip`](#content_tracks_items_clips_items_oneOf_i1)
            - [1.4.1.1.1.2.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > control`](#content_tracks_items_clips_items_oneOf_i1_control)
              - [1.4.1.1.1.2.1.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > control > gain`](#content_tracks_items_clips_items_oneOf_i1_control_gain)
              - [1.4.1.1.1.2.1.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > control > mute`](#content_tracks_items_clips_items_oneOf_i1_control_mute)
              - [1.4.1.1.1.2.1.3. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > control > pan`](#content_tracks_items_clips_items_oneOf_i1_control_pan)
            - [1.4.1.1.1.2.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > name`](#content_tracks_items_clips_items_oneOf_i1_name)
            - [1.4.1.1.1.2.3. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes`](#content_tracks_items_clips_items_oneOf_i1_notes)
              - [1.4.1.1.1.2.3.1. DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note](#content_tracks_items_clips_items_oneOf_i1_notes_items)
                - [1.4.1.1.1.2.3.1.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > centShift`](#content_tracks_items_clips_items_oneOf_i1_notes_items_centShift)
                - [1.4.1.1.1.2.3.1.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > keyNum`](#content_tracks_items_clips_items_oneOf_i1_notes_items_keyNum)
                - [1.4.1.1.1.2.3.1.3. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > language`](#content_tracks_items_clips_items_oneOf_i1_notes_items_language)
                - [1.4.1.1.1.2.3.1.4. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > length`](#content_tracks_items_clips_items_oneOf_i1_notes_items_length)
                - [1.4.1.1.1.2.3.1.5. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > lyric`](#content_tracks_items_clips_items_oneOf_i1_notes_items_lyric)
                - [1.4.1.1.1.2.3.1.6. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > phonemes`](#content_tracks_items_clips_items_oneOf_i1_notes_items_phonemes)
                  - [1.4.1.1.1.2.3.1.6.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > phonemes > edited`](#content_tracks_items_clips_items_oneOf_i1_notes_items_phonemes_edited)
                    - [1.4.1.1.1.2.3.1.6.1.1. DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > phonemes > edited > Phoneme](#content_tracks_items_clips_items_oneOf_i1_notes_items_phonemes_edited_items)
                      - [1.4.1.1.1.2.3.1.6.1.1.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > phonemes > edited > Phoneme > language`](#content_tracks_items_clips_items_oneOf_i1_notes_items_phonemes_edited_items_language)
                      - [1.4.1.1.1.2.3.1.6.1.1.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > phonemes > edited > Phoneme > start`](#content_tracks_items_clips_items_oneOf_i1_notes_items_phonemes_edited_items_start)
                      - [1.4.1.1.1.2.3.1.6.1.1.3. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > phonemes > edited > Phoneme > token`](#content_tracks_items_clips_items_oneOf_i1_notes_items_phonemes_edited_items_token)
                      - [1.4.1.1.1.2.3.1.6.1.1.4. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > phonemes > edited > Phoneme > onset`](#content_tracks_items_clips_items_oneOf_i1_notes_items_phonemes_edited_items_onset)
                  - [1.4.1.1.1.2.3.1.6.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > phonemes > original`](#content_tracks_items_clips_items_oneOf_i1_notes_items_phonemes_original)
                    - [1.4.1.1.1.2.3.1.6.2.1. DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > phonemes > original > Phoneme](#content_tracks_items_clips_items_oneOf_i1_notes_items_phonemes_original_items)
                      - [1.4.1.1.1.2.3.1.6.2.1.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > phonemes > original > Phoneme > language`](#content_tracks_items_clips_items_oneOf_i1_notes_items_phonemes_original_items_language)
                      - [1.4.1.1.1.2.3.1.6.2.1.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > phonemes > original > Phoneme > start`](#content_tracks_items_clips_items_oneOf_i1_notes_items_phonemes_original_items_start)
                      - [1.4.1.1.1.2.3.1.6.2.1.3. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > phonemes > original > Phoneme > token`](#content_tracks_items_clips_items_oneOf_i1_notes_items_phonemes_original_items_token)
                      - [1.4.1.1.1.2.3.1.6.2.1.4. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > phonemes > original > Phoneme > onset`](#content_tracks_items_clips_items_oneOf_i1_notes_items_phonemes_original_items_onset)
                - [1.4.1.1.1.2.3.1.7. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > pos`](#content_tracks_items_clips_items_oneOf_i1_notes_items_pos)
                - [1.4.1.1.1.2.3.1.8. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > pronunciation`](#content_tracks_items_clips_items_oneOf_i1_notes_items_pronunciation)
                  - [1.4.1.1.1.2.3.1.8.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > pronunciation > edited`](#content_tracks_items_clips_items_oneOf_i1_notes_items_pronunciation_edited)
                  - [1.4.1.1.1.2.3.1.8.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > pronunciation > original`](#content_tracks_items_clips_items_oneOf_i1_notes_items_pronunciation_original)
                - [1.4.1.1.1.2.3.1.9. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > vibrato`](#content_tracks_items_clips_items_oneOf_i1_notes_items_vibrato)
                  - [1.4.1.1.1.2.3.1.9.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > vibrato > amp`](#content_tracks_items_clips_items_oneOf_i1_notes_items_vibrato_amp)
                  - [1.4.1.1.1.2.3.1.9.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > vibrato > end`](#content_tracks_items_clips_items_oneOf_i1_notes_items_vibrato_end)
                  - [1.4.1.1.1.2.3.1.9.3. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > vibrato > freq`](#content_tracks_items_clips_items_oneOf_i1_notes_items_vibrato_freq)
                  - [1.4.1.1.1.2.3.1.9.4. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > vibrato > offset`](#content_tracks_items_clips_items_oneOf_i1_notes_items_vibrato_offset)
                  - [1.4.1.1.1.2.3.1.9.5. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > vibrato > phase`](#content_tracks_items_clips_items_oneOf_i1_notes_items_vibrato_phase)
                  - [1.4.1.1.1.2.3.1.9.6. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > vibrato > points`](#content_tracks_items_clips_items_oneOf_i1_notes_items_vibrato_points)
                    - [1.4.1.1.1.2.3.1.9.6.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > vibrato > points > amp`](#content_tracks_items_clips_items_oneOf_i1_notes_items_vibrato_points_amp)
                      - [1.4.1.1.1.2.3.1.9.6.1.1. DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > vibrato > points > amp > Control Point](#content_tracks_items_clips_items_oneOf_i1_notes_items_vibrato_points_amp_items)
                        - [1.4.1.1.1.2.3.1.9.6.1.1.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > vibrato > points > amp > Control Point > x`](#content_tracks_items_clips_items_oneOf_i1_notes_items_vibrato_points_amp_items_x)
                        - [1.4.1.1.1.2.3.1.9.6.1.1.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > vibrato > points > amp > Control Point > y`](#content_tracks_items_clips_items_oneOf_i1_notes_items_vibrato_points_amp_items_y)
                    - [1.4.1.1.1.2.3.1.9.6.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > vibrato > points > freq`](#content_tracks_items_clips_items_oneOf_i1_notes_items_vibrato_points_freq)
                      - [1.4.1.1.1.2.3.1.9.6.2.1. DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > vibrato > points > freq > Control Point](#content_tracks_items_clips_items_oneOf_i1_notes_items_vibrato_points_freq_items)
                        - [1.4.1.1.1.2.3.1.9.6.2.1.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > vibrato > points > freq > Control Point > x`](#content_tracks_items_clips_items_oneOf_i1_notes_items_vibrato_points_freq_items_x)
                        - [1.4.1.1.1.2.3.1.9.6.2.1.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > vibrato > points > freq > Control Point > y`](#content_tracks_items_clips_items_oneOf_i1_notes_items_vibrato_points_freq_items_y)
                  - [1.4.1.1.1.2.3.1.9.7. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > vibrato > start`](#content_tracks_items_clips_items_oneOf_i1_notes_items_vibrato_start)
                - [1.4.1.1.1.2.3.1.10. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > workspace`](#content_tracks_items_clips_items_oneOf_i1_notes_items_workspace)
                  - [1.4.1.1.1.2.3.1.10.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > workspace > Workspace Item`](#content_tracks_items_clips_items_oneOf_i1_notes_items_workspace_additionalProperties)
            - [1.4.1.1.1.2.4. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params`](#content_tracks_items_clips_items_oneOf_i1_params)
              - [1.4.1.1.1.2.4.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter`](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties)
                - [1.4.1.1.1.2.4.1.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > edited`](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_edited)
                  - [1.4.1.1.1.2.4.1.1.1. DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > edited > Parameter Curve](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_edited_items)
                    - [1.4.1.1.1.2.4.1.1.1.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > edited > Parameter Curve > oneOf > Anchor Parameter Curve`](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_edited_items_oneOf_i0)
                      - [1.4.1.1.1.2.4.1.1.1.1.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > edited > Parameter Curve > oneOf > Anchor Parameter Curve > nodes`](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_edited_items_oneOf_i0_nodes)
                        - [1.4.1.1.1.2.4.1.1.1.1.1.1. DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > edited > Parameter Curve > oneOf > Anchor Parameter Curve > nodes > Anchor Node](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_edited_items_oneOf_i0_nodes_items)
                          - [1.4.1.1.1.2.4.1.1.1.1.1.1.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > edited > Parameter Curve > oneOf > Anchor Parameter Curve > nodes > Anchor Node > interp`](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_edited_items_oneOf_i0_nodes_items_interp)
                          - [1.4.1.1.1.2.4.1.1.1.1.1.1.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > edited > Parameter Curve > oneOf > Anchor Parameter Curve > nodes > Anchor Node > x`](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_edited_items_oneOf_i0_nodes_items_x)
                          - [1.4.1.1.1.2.4.1.1.1.1.1.1.3. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > edited > Parameter Curve > oneOf > Anchor Parameter Curve > nodes > Anchor Node > y`](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_edited_items_oneOf_i0_nodes_items_y)
                      - [1.4.1.1.1.2.4.1.1.1.1.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > edited > Parameter Curve > oneOf > Anchor Parameter Curve > start`](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_edited_items_oneOf_i0_start)
                      - [1.4.1.1.1.2.4.1.1.1.1.3. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > edited > Parameter Curve > oneOf > Anchor Parameter Curve > type`](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_edited_items_oneOf_i0_type)
                    - [1.4.1.1.1.2.4.1.1.1.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > edited > Parameter Curve > oneOf > Free Parameter Curve`](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_edited_items_oneOf_i1)
                      - [1.4.1.1.1.2.4.1.1.1.2.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > edited > Parameter Curve > oneOf > Free Parameter Curve > start`](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_edited_items_oneOf_i1_start)
                      - [1.4.1.1.1.2.4.1.1.1.2.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > edited > Parameter Curve > oneOf > Free Parameter Curve > step`](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_edited_items_oneOf_i1_step)
                      - [1.4.1.1.1.2.4.1.1.1.2.3. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > edited > Parameter Curve > oneOf > Free Parameter Curve > type`](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_edited_items_oneOf_i1_type)
                      - [1.4.1.1.1.2.4.1.1.1.2.4. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > edited > Parameter Curve > oneOf > Free Parameter Curve > values`](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_edited_items_oneOf_i1_values)
                        - [1.4.1.1.1.2.4.1.1.1.2.4.1. DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > edited > Parameter Curve > oneOf > Free Parameter Curve > values > Parameter Value](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_edited_items_oneOf_i1_values_items)
                - [1.4.1.1.1.2.4.1.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > transform`](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_transform)
                  - [1.4.1.1.1.2.4.1.2.1. DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > transform > Parameter Curve](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_transform_items)
                    - [1.4.1.1.1.2.4.1.2.1.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > transform > Parameter Curve > oneOf > Anchor Parameter Curve`](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_transform_items_oneOf_i0)
                      - [1.4.1.1.1.2.4.1.2.1.1.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > transform > Parameter Curve > oneOf > Anchor Parameter Curve > nodes`](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_transform_items_oneOf_i0_nodes)
                        - [1.4.1.1.1.2.4.1.2.1.1.1.1. DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > transform > Parameter Curve > oneOf > Anchor Parameter Curve > nodes > Anchor Node](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_transform_items_oneOf_i0_nodes_items)
                          - [1.4.1.1.1.2.4.1.2.1.1.1.1.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > transform > Parameter Curve > oneOf > Anchor Parameter Curve > nodes > Anchor Node > interp`](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_transform_items_oneOf_i0_nodes_items_interp)
                          - [1.4.1.1.1.2.4.1.2.1.1.1.1.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > transform > Parameter Curve > oneOf > Anchor Parameter Curve > nodes > Anchor Node > x`](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_transform_items_oneOf_i0_nodes_items_x)
                          - [1.4.1.1.1.2.4.1.2.1.1.1.1.3. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > transform > Parameter Curve > oneOf > Anchor Parameter Curve > nodes > Anchor Node > y`](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_transform_items_oneOf_i0_nodes_items_y)
                      - [1.4.1.1.1.2.4.1.2.1.1.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > transform > Parameter Curve > oneOf > Anchor Parameter Curve > start`](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_transform_items_oneOf_i0_start)
                      - [1.4.1.1.1.2.4.1.2.1.1.3. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > transform > Parameter Curve > oneOf > Anchor Parameter Curve > type`](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_transform_items_oneOf_i0_type)
                    - [1.4.1.1.1.2.4.1.2.1.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > transform > Parameter Curve > oneOf > Free Parameter Curve`](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_transform_items_oneOf_i1)
                      - [1.4.1.1.1.2.4.1.2.1.2.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > transform > Parameter Curve > oneOf > Free Parameter Curve > start`](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_transform_items_oneOf_i1_start)
                      - [1.4.1.1.1.2.4.1.2.1.2.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > transform > Parameter Curve > oneOf > Free Parameter Curve > step`](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_transform_items_oneOf_i1_step)
                      - [1.4.1.1.1.2.4.1.2.1.2.3. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > transform > Parameter Curve > oneOf > Free Parameter Curve > type`](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_transform_items_oneOf_i1_type)
                      - [1.4.1.1.1.2.4.1.2.1.2.4. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > transform > Parameter Curve > oneOf > Free Parameter Curve > values`](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_transform_items_oneOf_i1_values)
                        - [1.4.1.1.1.2.4.1.2.1.2.4.1. DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > transform > Parameter Curve > oneOf > Free Parameter Curve > values > Parameter Value](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_transform_items_oneOf_i1_values_items)
                - [1.4.1.1.1.2.4.1.3. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > original`](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_original)
                  - [1.4.1.1.1.2.4.1.3.1. DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > original > Parameter Curve](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_original_items)
                    - [1.4.1.1.1.2.4.1.3.1.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > original > Parameter Curve > oneOf > Anchor Parameter Curve`](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_original_items_oneOf_i0)
                      - [1.4.1.1.1.2.4.1.3.1.1.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > original > Parameter Curve > oneOf > Anchor Parameter Curve > nodes`](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_original_items_oneOf_i0_nodes)
                        - [1.4.1.1.1.2.4.1.3.1.1.1.1. DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > original > Parameter Curve > oneOf > Anchor Parameter Curve > nodes > Anchor Node](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_original_items_oneOf_i0_nodes_items)
                          - [1.4.1.1.1.2.4.1.3.1.1.1.1.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > original > Parameter Curve > oneOf > Anchor Parameter Curve > nodes > Anchor Node > interp`](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_original_items_oneOf_i0_nodes_items_interp)
                          - [1.4.1.1.1.2.4.1.3.1.1.1.1.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > original > Parameter Curve > oneOf > Anchor Parameter Curve > nodes > Anchor Node > x`](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_original_items_oneOf_i0_nodes_items_x)
                          - [1.4.1.1.1.2.4.1.3.1.1.1.1.3. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > original > Parameter Curve > oneOf > Anchor Parameter Curve > nodes > Anchor Node > y`](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_original_items_oneOf_i0_nodes_items_y)
                      - [1.4.1.1.1.2.4.1.3.1.1.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > original > Parameter Curve > oneOf > Anchor Parameter Curve > start`](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_original_items_oneOf_i0_start)
                      - [1.4.1.1.1.2.4.1.3.1.1.3. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > original > Parameter Curve > oneOf > Anchor Parameter Curve > type`](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_original_items_oneOf_i0_type)
                    - [1.4.1.1.1.2.4.1.3.1.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > original > Parameter Curve > oneOf > Free Parameter Curve`](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_original_items_oneOf_i1)
                      - [1.4.1.1.1.2.4.1.3.1.2.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > original > Parameter Curve > oneOf > Free Parameter Curve > start`](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_original_items_oneOf_i1_start)
                      - [1.4.1.1.1.2.4.1.3.1.2.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > original > Parameter Curve > oneOf > Free Parameter Curve > step`](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_original_items_oneOf_i1_step)
                      - [1.4.1.1.1.2.4.1.3.1.2.3. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > original > Parameter Curve > oneOf > Free Parameter Curve > type`](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_original_items_oneOf_i1_type)
                      - [1.4.1.1.1.2.4.1.3.1.2.4. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > original > Parameter Curve > oneOf > Free Parameter Curve > values`](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_original_items_oneOf_i1_values)
                        - [1.4.1.1.1.2.4.1.3.1.2.4.1. DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > original > Parameter Curve > oneOf > Free Parameter Curve > values > Parameter Value](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_original_items_oneOf_i1_values_items)
            - [1.4.1.1.1.2.5. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > sources`](#content_tracks_items_clips_items_oneOf_i1_sources)
              - [1.4.1.1.1.2.5.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > sources > Source`](#content_tracks_items_clips_items_oneOf_i1_sources_additionalProperties)
            - [1.4.1.1.1.2.6. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > time`](#content_tracks_items_clips_items_oneOf_i1_time)
              - [1.4.1.1.1.2.6.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > time > clipLen`](#content_tracks_items_clips_items_oneOf_i1_time_clipLen)
              - [1.4.1.1.1.2.6.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > time > clipStart`](#content_tracks_items_clips_items_oneOf_i1_time_clipStart)
              - [1.4.1.1.1.2.6.3. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > time > length`](#content_tracks_items_clips_items_oneOf_i1_time_length)
              - [1.4.1.1.1.2.6.4. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > time > start`](#content_tracks_items_clips_items_oneOf_i1_time_start)
            - [1.4.1.1.1.2.7. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > type`](#content_tracks_items_clips_items_oneOf_i1_type)
            - [1.4.1.1.1.2.8. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > workspace`](#content_tracks_items_clips_items_oneOf_i1_workspace)
              - [1.4.1.1.1.2.8.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > workspace > Workspace Item`](#content_tracks_items_clips_items_oneOf_i1_workspace_additionalProperties)
      - [1.4.1.2. Property `DiffScope Project Exchange Format > content > tracks > Track > control`](#content_tracks_items_control)
        - [1.4.1.2.1. Property `DiffScope Project Exchange Format > content > tracks > Track > control > gain`](#content_tracks_items_control_gain)
        - [1.4.1.2.2. Property `DiffScope Project Exchange Format > content > tracks > Track > control > mute`](#content_tracks_items_control_mute)
        - [1.4.1.2.3. Property `DiffScope Project Exchange Format > content > tracks > Track > control > pan`](#content_tracks_items_control_pan)
        - [1.4.1.2.4. Property `DiffScope Project Exchange Format > content > tracks > Track > control > solo`](#content_tracks_items_control_solo)
      - [1.4.1.3. Property `DiffScope Project Exchange Format > content > tracks > Track > name`](#content_tracks_items_name)
      - [1.4.1.4. Property `DiffScope Project Exchange Format > content > tracks > Track > workspace`](#content_tracks_items_workspace)
        - [1.4.1.4.1. Property `DiffScope Project Exchange Format > content > tracks > Track > workspace > Workspace Item`](#content_tracks_items_workspace_additionalProperties)
  - [1.5. Property `DiffScope Project Exchange Format > content > workspace`](#content_workspace)
    - [1.5.1. Property `DiffScope Project Exchange Format > content > workspace > Workspace Item`](#content_workspace_additionalProperties)
- [2. Property `DiffScope Project Exchange Format > version`](#version)

**Title:** DiffScope Project Exchange Format

|                           |             |
| ------------------------- | ----------- |
| **Type**                  | `object`    |
| **Required**              | No          |
| **Additional properties** | Not allowed |

| Property               | Pattern | Type   | Deprecated | Definition | Title/Description |
| ---------------------- | ------- | ------ | ---------- | ---------- | ----------------- |
| + [content](#content ) | No      | object | No         | -          | Content           |
| + [version](#version ) | No      | const  | No         | -          | Version           |

## <a name="content"></a>1. Property `DiffScope Project Exchange Format > content`

**Title:** Content

|                           |             |
| ------------------------- | ----------- |
| **Type**                  | `object`    |
| **Required**              | Yes         |
| **Additional properties** | Not allowed |

| Property                           | Pattern | Type   | Deprecated | Definition           | Title/Description |
| ---------------------------------- | ------- | ------ | ---------- | -------------------- | ----------------- |
| + [global](#content_global )       | No      | object | No         | -                    | Global            |
| + [master](#content_master )       | No      | object | No         | -                    | Master            |
| + [timeline](#content_timeline )   | No      | object | No         | -                    | Timeline          |
| + [tracks](#content_tracks )       | No      | array  | No         | -                    | Tracks            |
| + [workspace](#content_workspace ) | No      | object | No         | In #/$defs/workspace | Workspace         |

### <a name="content_global"></a>1.1. Property `DiffScope Project Exchange Format > content > global`

**Title:** Global

|                           |             |
| ------------------------- | ----------- |
| **Type**                  | `object`    |
| **Required**              | Yes         |
| **Additional properties** | Not allowed |

**Description:** Global metadata for the project

| Property                                    | Pattern | Type    | Deprecated | Definition           | Title/Description |
| ------------------------------------------- | ------- | ------- | ---------- | -------------------- | ----------------- |
| + [author](#content_global_author )         | No      | string  | No         | -                    | Project Author    |
| + [centShift](#content_global_centShift )   | No      | integer | No         | In #/$defs/centShift | Cent Shift        |
| + [editorId](#content_global_editorId )     | No      | string  | No         | -                    | Editor Identifier |
| + [editorName](#content_global_editorName ) | No      | string  | No         | -                    | Editor Name       |
| + [name](#content_global_name )             | No      | string  | No         | -                    | Project Name      |

#### <a name="content_global_author"></a>1.1.1. Property `DiffScope Project Exchange Format > content > global > author`

**Title:** Project Author

|              |          |
| ------------ | -------- |
| **Type**     | `string` |
| **Required** | Yes      |

#### <a name="content_global_centShift"></a>1.1.2. Property `DiffScope Project Exchange Format > content > global > centShift`

**Title:** Cent Shift

|                |                   |
| -------------- | ----------------- |
| **Type**       | `integer`         |
| **Required**   | Yes               |
| **Defined in** | #/$defs/centShift |

| Restrictions |          |
| ------------ | -------- |
| **Minimum**  | &ge; -50 |
| **Maximum**  | &le; 50  |

#### <a name="content_global_editorId"></a>1.1.3. Property `DiffScope Project Exchange Format > content > global > editorId`

**Title:** Editor Identifier

|              |          |
| ------------ | -------- |
| **Type**     | `string` |
| **Required** | Yes      |

#### <a name="content_global_editorName"></a>1.1.4. Property `DiffScope Project Exchange Format > content > global > editorName`

**Title:** Editor Name

|              |          |
| ------------ | -------- |
| **Type**     | `string` |
| **Required** | Yes      |

#### <a name="content_global_name"></a>1.1.5. Property `DiffScope Project Exchange Format > content > global > name`

**Title:** Project Name

|              |          |
| ------------ | -------- |
| **Type**     | `string` |
| **Required** | Yes      |

### <a name="content_master"></a>1.2. Property `DiffScope Project Exchange Format > content > master`

**Title:** Master

|                           |             |
| ------------------------- | ----------- |
| **Type**                  | `object`    |
| **Required**              | Yes         |
| **Additional properties** | Not allowed |

| Property                              | Pattern | Type   | Deprecated | Definition            | Title/Description |
| ------------------------------------- | ------- | ------ | ---------- | --------------------- | ----------------- |
| + [control](#content_master_control ) | No      | object | No         | In #/$defs/busControl | Bus Control       |

#### <a name="content_master_control"></a>1.2.1. Property `DiffScope Project Exchange Format > content > master > control`

**Title:** Bus Control

|                           |                    |
| ------------------------- | ------------------ |
| **Type**                  | `object`           |
| **Required**              | Yes                |
| **Additional properties** | Not allowed        |
| **Defined in**            | #/$defs/busControl |

| Property                                | Pattern | Type    | Deprecated | Definition | Title/Description |
| --------------------------------------- | ------- | ------- | ---------- | ---------- | ----------------- |
| + [gain](#content_master_control_gain ) | No      | number  | No         | -          | Gain              |
| + [mute](#content_master_control_mute ) | No      | boolean | No         | -          | Mute              |
| + [pan](#content_master_control_pan )   | No      | number  | No         | -          | Pan               |

##### <a name="content_master_control_gain"></a>1.2.1.1. Property `DiffScope Project Exchange Format > content > master > control > gain`

**Title:** Gain

|              |          |
| ------------ | -------- |
| **Type**     | `number` |
| **Required** | Yes      |

##### <a name="content_master_control_mute"></a>1.2.1.2. Property `DiffScope Project Exchange Format > content > master > control > mute`

**Title:** Mute

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | Yes       |

##### <a name="content_master_control_pan"></a>1.2.1.3. Property `DiffScope Project Exchange Format > content > master > control > pan`

**Title:** Pan

|              |          |
| ------------ | -------- |
| **Type**     | `number` |
| **Required** | Yes      |

| Restrictions |         |
| ------------ | ------- |
| **Minimum**  | &ge; -1 |
| **Maximum**  | &le; 1  |

### <a name="content_timeline"></a>1.3. Property `DiffScope Project Exchange Format > content > timeline`

**Title:** Timeline

|                           |             |
| ------------------------- | ----------- |
| **Type**                  | `object`    |
| **Required**              | Yes         |
| **Additional properties** | Not allowed |

| Property                                              | Pattern | Type  | Deprecated | Definition | Title/Description |
| ----------------------------------------------------- | ------- | ----- | ---------- | ---------- | ----------------- |
| + [labels](#content_timeline_labels )                 | No      | array | No         | -          | Labels            |
| + [tempos](#content_timeline_tempos )                 | No      | array | No         | -          | Tempos            |
| + [timeSignatures](#content_timeline_timeSignatures ) | No      | array | No         | -          | Time Signatures   |

#### <a name="content_timeline_labels"></a>1.3.1. Property `DiffScope Project Exchange Format > content > timeline > labels`

**Title:** Labels

|              |         |
| ------------ | ------- |
| **Type**     | `array` |
| **Required** | Yes     |

|                      | Array restrictions |
| -------------------- | ------------------ |
| **Min items**        | N/A                |
| **Max items**        | N/A                |
| **Items unicity**    | False              |
| **Additional items** | False              |
| **Tuple validation** | See below          |

| Each item of this array must be         | Description |
| --------------------------------------- | ----------- |
| [Label](#content_timeline_labels_items) | -           |

##### <a name="content_timeline_labels_items"></a>1.3.1.1. DiffScope Project Exchange Format > content > timeline > labels > Label

**Title:** Label

|                           |               |
| ------------------------- | ------------- |
| **Type**                  | `object`      |
| **Required**              | No            |
| **Additional properties** | Not allowed   |
| **Defined in**            | #/$defs/label |

| Property                                       | Pattern | Type    | Deprecated | Definition | Title/Description |
| ---------------------------------------------- | ------- | ------- | ---------- | ---------- | ----------------- |
| + [pos](#content_timeline_labels_items_pos )   | No      | integer | No         | -          | Position (Ticks)  |
| + [text](#content_timeline_labels_items_text ) | No      | string  | No         | -          | Text              |

###### <a name="content_timeline_labels_items_pos"></a>1.3.1.1.1. Property `DiffScope Project Exchange Format > content > timeline > labels > Label > pos`

**Title:** Position (Ticks)

|              |           |
| ------------ | --------- |
| **Type**     | `integer` |
| **Required** | Yes       |

| Restrictions |                 |
| ------------ | --------------- |
| **Minimum**  | &ge; 0          |
| **Maximum**  | &le; 2147483647 |

###### <a name="content_timeline_labels_items_text"></a>1.3.1.1.2. Property `DiffScope Project Exchange Format > content > timeline > labels > Label > text`

**Title:** Text

|              |          |
| ------------ | -------- |
| **Type**     | `string` |
| **Required** | Yes      |

#### <a name="content_timeline_tempos"></a>1.3.2. Property `DiffScope Project Exchange Format > content > timeline > tempos`

**Title:** Tempos

|              |         |
| ------------ | ------- |
| **Type**     | `array` |
| **Required** | Yes     |

|                      | Array restrictions |
| -------------------- | ------------------ |
| **Min items**        | N/A                |
| **Max items**        | N/A                |
| **Items unicity**    | False              |
| **Additional items** | False              |
| **Tuple validation** | See below          |

| Each item of this array must be         | Description |
| --------------------------------------- | ----------- |
| [Tempo](#content_timeline_tempos_items) | -           |

##### <a name="content_timeline_tempos_items"></a>1.3.2.1. DiffScope Project Exchange Format > content > timeline > tempos > Tempo

**Title:** Tempo

|                           |               |
| ------------------------- | ------------- |
| **Type**                  | `object`      |
| **Required**              | No            |
| **Additional properties** | Not allowed   |
| **Defined in**            | #/$defs/tempo |

| Property                                         | Pattern | Type    | Deprecated | Definition | Title/Description |
| ------------------------------------------------ | ------- | ------- | ---------- | ---------- | ----------------- |
| + [pos](#content_timeline_tempos_items_pos )     | No      | integer | No         | -          | Position (Ticks)  |
| + [value](#content_timeline_tempos_items_value ) | No      | number  | No         | -          | Tempo Value       |

###### <a name="content_timeline_tempos_items_pos"></a>1.3.2.1.1. Property `DiffScope Project Exchange Format > content > timeline > tempos > Tempo > pos`

**Title:** Position (Ticks)

|              |           |
| ------------ | --------- |
| **Type**     | `integer` |
| **Required** | Yes       |

| Restrictions |                 |
| ------------ | --------------- |
| **Minimum**  | &ge; 0          |
| **Maximum**  | &le; 2147483647 |

###### <a name="content_timeline_tempos_items_value"></a>1.3.2.1.2. Property `DiffScope Project Exchange Format > content > timeline > tempos > Tempo > value`

**Title:** Tempo Value

|              |          |
| ------------ | -------- |
| **Type**     | `number` |
| **Required** | Yes      |

**Description:** Quarter notes per minute

| Restrictions |           |
| ------------ | --------- |
| **Minimum**  | &ge; 10   |
| **Maximum**  | &le; 1000 |

#### <a name="content_timeline_timeSignatures"></a>1.3.3. Property `DiffScope Project Exchange Format > content > timeline > timeSignatures`

**Title:** Time Signatures

|              |         |
| ------------ | ------- |
| **Type**     | `array` |
| **Required** | Yes     |

|                      | Array restrictions |
| -------------------- | ------------------ |
| **Min items**        | N/A                |
| **Max items**        | N/A                |
| **Items unicity**    | False              |
| **Additional items** | False              |
| **Tuple validation** | See below          |

| Each item of this array must be                          | Description |
| -------------------------------------------------------- | ----------- |
| [Time Signature](#content_timeline_timeSignatures_items) | -           |

##### <a name="content_timeline_timeSignatures_items"></a>1.3.3.1. DiffScope Project Exchange Format > content > timeline > timeSignatures > Time Signature

**Title:** Time Signature

|                           |                       |
| ------------------------- | --------------------- |
| **Type**                  | `object`              |
| **Required**              | No                    |
| **Additional properties** | Not allowed           |
| **Defined in**            | #/$defs/timeSignature |

| Property                                                             | Pattern | Type              | Deprecated | Definition | Title/Description        |
| -------------------------------------------------------------------- | ------- | ----------------- | ---------- | ---------- | ------------------------ |
| + [denominator](#content_timeline_timeSignatures_items_denominator ) | No      | enum (of integer) | No         | -          | Denominator              |
| + [index](#content_timeline_timeSignatures_items_index )             | No      | integer           | No         | -          | Measure number (0-based) |
| + [numerator](#content_timeline_timeSignatures_items_numerator )     | No      | integer           | No         | -          | Numerator                |

###### <a name="content_timeline_timeSignatures_items_denominator"></a>1.3.3.1.1. Property `DiffScope Project Exchange Format > content > timeline > timeSignatures > Time Signature > denominator`

**Title:** Denominator

|              |                     |
| ------------ | ------------------- |
| **Type**     | `enum (of integer)` |
| **Required** | Yes                 |

Must be one of:
* 1
* 2
* 4
* 8
* 16
* 32
* 64
* 128

###### <a name="content_timeline_timeSignatures_items_index"></a>1.3.3.1.2. Property `DiffScope Project Exchange Format > content > timeline > timeSignatures > Time Signature > index`

**Title:** Measure number (0-based)

|              |           |
| ------------ | --------- |
| **Type**     | `integer` |
| **Required** | Yes       |

| Restrictions |                 |
| ------------ | --------------- |
| **Minimum**  | &ge; 0          |
| **Maximum**  | &le; 2147483647 |

###### <a name="content_timeline_timeSignatures_items_numerator"></a>1.3.3.1.3. Property `DiffScope Project Exchange Format > content > timeline > timeSignatures > Time Signature > numerator`

**Title:** Numerator

|              |           |
| ------------ | --------- |
| **Type**     | `integer` |
| **Required** | Yes       |

| Restrictions |                 |
| ------------ | --------------- |
| **Minimum**  | &ge; 1          |
| **Maximum**  | &le; 2147483647 |

### <a name="content_tracks"></a>1.4. Property `DiffScope Project Exchange Format > content > tracks`

**Title:** Tracks

|              |         |
| ------------ | ------- |
| **Type**     | `array` |
| **Required** | Yes     |

|                      | Array restrictions |
| -------------------- | ------------------ |
| **Min items**        | N/A                |
| **Max items**        | N/A                |
| **Items unicity**    | False              |
| **Additional items** | False              |
| **Tuple validation** | See below          |

| Each item of this array must be | Description |
| ------------------------------- | ----------- |
| [Track](#content_tracks_items)  | -           |

#### <a name="content_tracks_items"></a>1.4.1. DiffScope Project Exchange Format > content > tracks > Track

**Title:** Track

|                           |               |
| ------------------------- | ------------- |
| **Type**                  | `object`      |
| **Required**              | No            |
| **Additional properties** | Not allowed   |
| **Defined in**            | #/$defs/track |

| Property                                        | Pattern | Type   | Deprecated | Definition              | Title/Description |
| ----------------------------------------------- | ------- | ------ | ---------- | ----------------------- | ----------------- |
| + [clips](#content_tracks_items_clips )         | No      | array  | No         | -                       | Clips             |
| + [control](#content_tracks_items_control )     | No      | object | No         | In #/$defs/trackControl | Track Control     |
| + [name](#content_tracks_items_name )           | No      | string | No         | -                       | Track Name        |
| + [workspace](#content_tracks_items_workspace ) | No      | object | No         | In #/$defs/workspace    | Workspace         |

##### <a name="content_tracks_items_clips"></a>1.4.1.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips`

**Title:** Clips

|              |         |
| ------------ | ------- |
| **Type**     | `array` |
| **Required** | Yes     |

|                      | Array restrictions |
| -------------------- | ------------------ |
| **Min items**        | N/A                |
| **Max items**        | N/A                |
| **Items unicity**    | False              |
| **Additional items** | False              |
| **Tuple validation** | See below          |

| Each item of this array must be           | Description |
| ----------------------------------------- | ----------- |
| [Clip](#content_tracks_items_clips_items) | -           |

###### <a name="content_tracks_items_clips_items"></a>1.4.1.1.1. DiffScope Project Exchange Format > content > tracks > Track > clips > Clip

**Title:** Clip

|                           |                  |
| ------------------------- | ---------------- |
| **Type**                  | `combining`      |
| **Required**              | No               |
| **Additional properties** | Any type allowed |
| **Defined in**            | #/$defs/clip     |

| One of(Option)                                             |
| ---------------------------------------------------------- |
| [Audio Clip](#content_tracks_items_clips_items_oneOf_i0)   |
| [Singing Clip](#content_tracks_items_clips_items_oneOf_i1) |

###### <a name="content_tracks_items_clips_items_oneOf_i0"></a>1.4.1.1.1.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Audio Clip`

**Title:** Audio Clip

|                           |                   |
| ------------------------- | ----------------- |
| **Type**                  | `object`          |
| **Required**              | No                |
| **Additional properties** | Not allowed       |
| **Defined in**            | #/$defs/audioClip |

| Property                                                             | Pattern | Type   | Deprecated | Definition            | Title/Description |
| -------------------------------------------------------------------- | ------- | ------ | ---------- | --------------------- | ----------------- |
| + [control](#content_tracks_items_clips_items_oneOf_i0_control )     | No      | object | No         | In #/$defs/busControl | Bus Control       |
| + [name](#content_tracks_items_clips_items_oneOf_i0_name )           | No      | string | No         | -                     | Clip Name         |
| + [path](#content_tracks_items_clips_items_oneOf_i0_path )           | No      | string | No         | -                     | Audio File Path   |
| + [time](#content_tracks_items_clips_items_oneOf_i0_time )           | No      | object | No         | In #/$defs/clipTime   | Clip Time         |
| + [type](#content_tracks_items_clips_items_oneOf_i0_type )           | No      | const  | No         | -                     | Clip Type         |
| + [workspace](#content_tracks_items_clips_items_oneOf_i0_workspace ) | No      | object | No         | In #/$defs/workspace  | Workspace         |

###### <a name="content_tracks_items_clips_items_oneOf_i0_control"></a>1.4.1.1.1.1.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Audio Clip > control`

**Title:** Bus Control

|                           |                    |
| ------------------------- | ------------------ |
| **Type**                  | `object`           |
| **Required**              | Yes                |
| **Additional properties** | Not allowed        |
| **Defined in**            | #/$defs/busControl |

| Property                                                           | Pattern | Type    | Deprecated | Definition | Title/Description |
| ------------------------------------------------------------------ | ------- | ------- | ---------- | ---------- | ----------------- |
| + [gain](#content_tracks_items_clips_items_oneOf_i0_control_gain ) | No      | number  | No         | -          | Gain              |
| + [mute](#content_tracks_items_clips_items_oneOf_i0_control_mute ) | No      | boolean | No         | -          | Mute              |
| + [pan](#content_tracks_items_clips_items_oneOf_i0_control_pan )   | No      | number  | No         | -          | Pan               |

###### <a name="content_tracks_items_clips_items_oneOf_i0_control_gain"></a>1.4.1.1.1.1.1.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Audio Clip > control > gain`

**Title:** Gain

|              |          |
| ------------ | -------- |
| **Type**     | `number` |
| **Required** | Yes      |

###### <a name="content_tracks_items_clips_items_oneOf_i0_control_mute"></a>1.4.1.1.1.1.1.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Audio Clip > control > mute`

**Title:** Mute

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | Yes       |

###### <a name="content_tracks_items_clips_items_oneOf_i0_control_pan"></a>1.4.1.1.1.1.1.3. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Audio Clip > control > pan`

**Title:** Pan

|              |          |
| ------------ | -------- |
| **Type**     | `number` |
| **Required** | Yes      |

| Restrictions |         |
| ------------ | ------- |
| **Minimum**  | &ge; -1 |
| **Maximum**  | &le; 1  |

###### <a name="content_tracks_items_clips_items_oneOf_i0_name"></a>1.4.1.1.1.1.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Audio Clip > name`

**Title:** Clip Name

|              |          |
| ------------ | -------- |
| **Type**     | `string` |
| **Required** | Yes      |

###### <a name="content_tracks_items_clips_items_oneOf_i0_path"></a>1.4.1.1.1.1.3. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Audio Clip > path`

**Title:** Audio File Path

|              |          |
| ------------ | -------- |
| **Type**     | `string` |
| **Required** | Yes      |

###### <a name="content_tracks_items_clips_items_oneOf_i0_time"></a>1.4.1.1.1.1.4. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Audio Clip > time`

**Title:** Clip Time

|                           |                  |
| ------------------------- | ---------------- |
| **Type**                  | `object`         |
| **Required**              | Yes              |
| **Additional properties** | Not allowed      |
| **Defined in**            | #/$defs/clipTime |

| Property                                                                  | Pattern | Type    | Deprecated | Definition | Title/Description      |
| ------------------------------------------------------------------------- | ------- | ------- | ---------- | ---------- | ---------------------- |
| + [clipLen](#content_tracks_items_clips_items_oneOf_i0_time_clipLen )     | No      | integer | No         | -          | Clipped Length (Ticks) |
| + [clipStart](#content_tracks_items_clips_items_oneOf_i0_time_clipStart ) | No      | integer | No         | -          | Clipped Start (Ticks)  |
| + [length](#content_tracks_items_clips_items_oneOf_i0_time_length )       | No      | integer | No         | -          | Length (Ticks)         |
| + [start](#content_tracks_items_clips_items_oneOf_i0_time_start )         | No      | integer | No         | -          | Start Position (Ticks) |

###### <a name="content_tracks_items_clips_items_oneOf_i0_time_clipLen"></a>1.4.1.1.1.1.4.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Audio Clip > time > clipLen`

**Title:** Clipped Length (Ticks)

|              |           |
| ------------ | --------- |
| **Type**     | `integer` |
| **Required** | Yes       |

**Description:** The clipped length relative to `clipStart`

| Restrictions |                 |
| ------------ | --------------- |
| **Minimum**  | &ge; 0          |
| **Maximum**  | &le; 2147483647 |

###### <a name="content_tracks_items_clips_items_oneOf_i0_time_clipStart"></a>1.4.1.1.1.1.4.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Audio Clip > time > clipStart`

**Title:** Clipped Start (Ticks)

|              |           |
| ------------ | --------- |
| **Type**     | `integer` |
| **Required** | Yes       |

**Description:** The clipped length relative to `start`

| Restrictions |                 |
| ------------ | --------------- |
| **Minimum**  | &ge; 0          |
| **Maximum**  | &le; 2147483647 |

###### <a name="content_tracks_items_clips_items_oneOf_i0_time_length"></a>1.4.1.1.1.1.4.3. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Audio Clip > time > length`

**Title:** Length (Ticks)

|              |           |
| ------------ | --------- |
| **Type**     | `integer` |
| **Required** | Yes       |

**Description:** The actual length of the content in the clip

| Restrictions |                 |
| ------------ | --------------- |
| **Minimum**  | &ge; 0          |
| **Maximum**  | &le; 2147483647 |

###### <a name="content_tracks_items_clips_items_oneOf_i0_time_start"></a>1.4.1.1.1.1.4.4. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Audio Clip > time > start`

**Title:** Start Position (Ticks)

|              |           |
| ------------ | --------- |
| **Type**     | `integer` |
| **Required** | Yes       |

**Description:** The start position of the content in the clip in the timeline

| Restrictions |                  |
| ------------ | ---------------- |
| **Minimum**  | &ge; -2147483648 |
| **Maximum**  | &le; 2147483647  |

###### <a name="content_tracks_items_clips_items_oneOf_i0_type"></a>1.4.1.1.1.1.5. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Audio Clip > type`

**Title:** Clip Type

|              |         |
| ------------ | ------- |
| **Type**     | `const` |
| **Required** | Yes     |

Specific value: `"audio"`

###### <a name="content_tracks_items_clips_items_oneOf_i0_workspace"></a>1.4.1.1.1.1.6. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Audio Clip > workspace`

**Title:** Workspace

|                           |                                                                                                                                  |
| ------------------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| **Type**                  | `object`                                                                                                                         |
| **Required**              | Yes                                                                                                                              |
| **Additional properties** | [Each additional property must conform to the schema](#content_tracks_items_clips_items_oneOf_i0_workspace_additionalProperties) |
| **Defined in**            | #/$defs/workspace                                                                                                                |

**Description:** A flexible object for storing application-specific data.

| Property                                                                         | Pattern | Type   | Deprecated | Definition | Title/Description |
| -------------------------------------------------------------------------------- | ------- | ------ | ---------- | ---------- | ----------------- |
| - [](#content_tracks_items_clips_items_oneOf_i0_workspace_additionalProperties ) | No      | object | No         | -          | Workspace Item    |

###### <a name="content_tracks_items_clips_items_oneOf_i0_workspace_additionalProperties"></a>1.4.1.1.1.1.6.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Audio Clip > workspace > Workspace Item`

**Title:** Workspace Item

|                           |                  |
| ------------------------- | ---------------- |
| **Type**                  | `object`         |
| **Required**              | No               |
| **Additional properties** | Any type allowed |

###### <a name="content_tracks_items_clips_items_oneOf_i1"></a>1.4.1.1.1.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip`

**Title:** Singing Clip

|                           |                     |
| ------------------------- | ------------------- |
| **Type**                  | `object`            |
| **Required**              | No                  |
| **Additional properties** | Not allowed         |
| **Defined in**            | #/$defs/singingClip |

| Property                                                             | Pattern | Type   | Deprecated | Definition            | Title/Description |
| -------------------------------------------------------------------- | ------- | ------ | ---------- | --------------------- | ----------------- |
| + [control](#content_tracks_items_clips_items_oneOf_i1_control )     | No      | object | No         | In #/$defs/busControl | Bus Control       |
| + [name](#content_tracks_items_clips_items_oneOf_i1_name )           | No      | string | No         | -                     | Clip Name         |
| + [notes](#content_tracks_items_clips_items_oneOf_i1_notes )         | No      | array  | No         | -                     | Notes             |
| + [params](#content_tracks_items_clips_items_oneOf_i1_params )       | No      | object | No         | -                     | Parameters        |
| + [sources](#content_tracks_items_clips_items_oneOf_i1_sources )     | No      | object | No         | -                     | Sources           |
| + [time](#content_tracks_items_clips_items_oneOf_i1_time )           | No      | object | No         | In #/$defs/clipTime   | Clip Time         |
| + [type](#content_tracks_items_clips_items_oneOf_i1_type )           | No      | const  | No         | -                     | Clip Type         |
| + [workspace](#content_tracks_items_clips_items_oneOf_i1_workspace ) | No      | object | No         | In #/$defs/workspace  | Workspace         |

###### <a name="content_tracks_items_clips_items_oneOf_i1_control"></a>1.4.1.1.1.2.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > control`

**Title:** Bus Control

|                           |                    |
| ------------------------- | ------------------ |
| **Type**                  | `object`           |
| **Required**              | Yes                |
| **Additional properties** | Not allowed        |
| **Defined in**            | #/$defs/busControl |

| Property                                                           | Pattern | Type    | Deprecated | Definition | Title/Description |
| ------------------------------------------------------------------ | ------- | ------- | ---------- | ---------- | ----------------- |
| + [gain](#content_tracks_items_clips_items_oneOf_i1_control_gain ) | No      | number  | No         | -          | Gain              |
| + [mute](#content_tracks_items_clips_items_oneOf_i1_control_mute ) | No      | boolean | No         | -          | Mute              |
| + [pan](#content_tracks_items_clips_items_oneOf_i1_control_pan )   | No      | number  | No         | -          | Pan               |

###### <a name="content_tracks_items_clips_items_oneOf_i1_control_gain"></a>1.4.1.1.1.2.1.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > control > gain`

**Title:** Gain

|              |          |
| ------------ | -------- |
| **Type**     | `number` |
| **Required** | Yes      |

###### <a name="content_tracks_items_clips_items_oneOf_i1_control_mute"></a>1.4.1.1.1.2.1.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > control > mute`

**Title:** Mute

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | Yes       |

###### <a name="content_tracks_items_clips_items_oneOf_i1_control_pan"></a>1.4.1.1.1.2.1.3. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > control > pan`

**Title:** Pan

|              |          |
| ------------ | -------- |
| **Type**     | `number` |
| **Required** | Yes      |

| Restrictions |         |
| ------------ | ------- |
| **Minimum**  | &ge; -1 |
| **Maximum**  | &le; 1  |

###### <a name="content_tracks_items_clips_items_oneOf_i1_name"></a>1.4.1.1.1.2.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > name`

**Title:** Clip Name

|              |          |
| ------------ | -------- |
| **Type**     | `string` |
| **Required** | Yes      |

###### <a name="content_tracks_items_clips_items_oneOf_i1_notes"></a>1.4.1.1.1.2.3. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes`

**Title:** Notes

|              |         |
| ------------ | ------- |
| **Type**     | `array` |
| **Required** | Yes     |

|                      | Array restrictions |
| -------------------- | ------------------ |
| **Min items**        | N/A                |
| **Max items**        | N/A                |
| **Items unicity**    | False              |
| **Additional items** | False              |
| **Tuple validation** | See below          |

| Each item of this array must be                                | Description |
| -------------------------------------------------------------- | ----------- |
| [Note](#content_tracks_items_clips_items_oneOf_i1_notes_items) | -           |

###### <a name="content_tracks_items_clips_items_oneOf_i1_notes_items"></a>1.4.1.1.1.2.3.1. DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note

**Title:** Note

|                           |              |
| ------------------------- | ------------ |
| **Type**                  | `object`     |
| **Required**              | No           |
| **Additional properties** | Not allowed  |
| **Defined in**            | #/$defs/note |

| Property                                                                                 | Pattern | Type    | Deprecated | Definition           | Title/Description         |
| ---------------------------------------------------------------------------------------- | ------- | ------- | ---------- | -------------------- | ------------------------- |
| + [centShift](#content_tracks_items_clips_items_oneOf_i1_notes_items_centShift )         | No      | integer | No         | In #/$defs/centShift | Cent Shift                |
| + [keyNum](#content_tracks_items_clips_items_oneOf_i1_notes_items_keyNum )               | No      | integer | No         | -                    | MIDI Key Number           |
| + [language](#content_tracks_items_clips_items_oneOf_i1_notes_items_language )           | No      | string  | No         | -                    | Language (ISO 639-3 Code) |
| + [length](#content_tracks_items_clips_items_oneOf_i1_notes_items_length )               | No      | integer | No         | -                    | Length (Ticks)            |
| + [lyric](#content_tracks_items_clips_items_oneOf_i1_notes_items_lyric )                 | No      | string  | No         | -                    | Lyric                     |
| + [phonemes](#content_tracks_items_clips_items_oneOf_i1_notes_items_phonemes )           | No      | object  | No         | -                    | Phonemes                  |
| + [pos](#content_tracks_items_clips_items_oneOf_i1_notes_items_pos )                     | No      | integer | No         | -                    | Position (Ticks)          |
| + [pronunciation](#content_tracks_items_clips_items_oneOf_i1_notes_items_pronunciation ) | No      | object  | No         | -                    | Pronunciation             |
| + [vibrato](#content_tracks_items_clips_items_oneOf_i1_notes_items_vibrato )             | No      | object  | No         | -                    | Vibrato                   |
| + [workspace](#content_tracks_items_clips_items_oneOf_i1_notes_items_workspace )         | No      | object  | No         | In #/$defs/workspace | Workspace                 |

###### <a name="content_tracks_items_clips_items_oneOf_i1_notes_items_centShift"></a>1.4.1.1.1.2.3.1.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > centShift`

**Title:** Cent Shift

|                |                   |
| -------------- | ----------------- |
| **Type**       | `integer`         |
| **Required**   | Yes               |
| **Defined in** | #/$defs/centShift |

| Restrictions |          |
| ------------ | -------- |
| **Minimum**  | &ge; -50 |
| **Maximum**  | &le; 50  |

###### <a name="content_tracks_items_clips_items_oneOf_i1_notes_items_keyNum"></a>1.4.1.1.1.2.3.1.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > keyNum`

**Title:** MIDI Key Number

|              |           |
| ------------ | --------- |
| **Type**     | `integer` |
| **Required** | Yes       |

| Restrictions |          |
| ------------ | -------- |
| **Minimum**  | &ge; 0   |
| **Maximum**  | &le; 127 |

###### <a name="content_tracks_items_clips_items_oneOf_i1_notes_items_language"></a>1.4.1.1.1.2.3.1.3. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > language`

**Title:** Language (ISO 639-3 Code)

|              |          |
| ------------ | -------- |
| **Type**     | `string` |
| **Required** | Yes      |

###### <a name="content_tracks_items_clips_items_oneOf_i1_notes_items_length"></a>1.4.1.1.1.2.3.1.4. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > length`

**Title:** Length (Ticks)

|              |           |
| ------------ | --------- |
| **Type**     | `integer` |
| **Required** | Yes       |

| Restrictions |                 |
| ------------ | --------------- |
| **Minimum**  | &ge; 0          |
| **Maximum**  | &le; 2147483647 |

###### <a name="content_tracks_items_clips_items_oneOf_i1_notes_items_lyric"></a>1.4.1.1.1.2.3.1.5. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > lyric`

**Title:** Lyric

|              |          |
| ------------ | -------- |
| **Type**     | `string` |
| **Required** | Yes      |

###### <a name="content_tracks_items_clips_items_oneOf_i1_notes_items_phonemes"></a>1.4.1.1.1.2.3.1.6. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > phonemes`

**Title:** Phonemes

|                           |             |
| ------------------------- | ----------- |
| **Type**                  | `object`    |
| **Required**              | Yes         |
| **Additional properties** | Not allowed |

| Property                                                                                | Pattern | Type  | Deprecated | Definition | Title/Description                              |
| --------------------------------------------------------------------------------------- | ------- | ----- | ---------- | ---------- | ---------------------------------------------- |
| + [edited](#content_tracks_items_clips_items_oneOf_i1_notes_items_phonemes_edited )     | No      | array | No         | -          | Edited Phonemes                                |
| + [original](#content_tracks_items_clips_items_oneOf_i1_notes_items_phonemes_original ) | No      | array | No         | -          | Original Phonemes Generated from Pronunciation |

###### <a name="content_tracks_items_clips_items_oneOf_i1_notes_items_phonemes_edited"></a>1.4.1.1.1.2.3.1.6.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > phonemes > edited`

**Title:** Edited Phonemes

|              |         |
| ------------ | ------- |
| **Type**     | `array` |
| **Required** | Yes     |

|                      | Array restrictions |
| -------------------- | ------------------ |
| **Min items**        | N/A                |
| **Max items**        | N/A                |
| **Items unicity**    | False              |
| **Additional items** | False              |
| **Tuple validation** | See below          |

| Each item of this array must be                                                         | Description |
| --------------------------------------------------------------------------------------- | ----------- |
| [Phoneme](#content_tracks_items_clips_items_oneOf_i1_notes_items_phonemes_edited_items) | -           |

###### <a name="content_tracks_items_clips_items_oneOf_i1_notes_items_phonemes_edited_items"></a>1.4.1.1.1.2.3.1.6.1.1. DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > phonemes > edited > Phoneme

**Title:** Phoneme

|                           |                 |
| ------------------------- | --------------- |
| **Type**                  | `object`        |
| **Required**              | No              |
| **Additional properties** | Not allowed     |
| **Defined in**            | #/$defs/phoneme |

| Property                                                                                             | Pattern | Type    | Deprecated | Definition | Title/Description                          |
| ---------------------------------------------------------------------------------------------------- | ------- | ------- | ---------- | ---------- | ------------------------------------------ |
| + [language](#content_tracks_items_clips_items_oneOf_i1_notes_items_phonemes_edited_items_language ) | No      | string  | No         | -          | Language (ISO 639-3 Code)                  |
| + [start](#content_tracks_items_clips_items_oneOf_i1_notes_items_phonemes_edited_items_start )       | No      | integer | No         | -          | Start Position (Milliseconds from Note On) |
| + [token](#content_tracks_items_clips_items_oneOf_i1_notes_items_phonemes_edited_items_token )       | No      | string  | No         | -          | Phoneme Token                              |
| + [onset](#content_tracks_items_clips_items_oneOf_i1_notes_items_phonemes_edited_items_onset )       | No      | boolean | No         | -          | Onset Flag                                 |

###### <a name="content_tracks_items_clips_items_oneOf_i1_notes_items_phonemes_edited_items_language"></a>1.4.1.1.1.2.3.1.6.1.1.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > phonemes > edited > Phoneme > language`

**Title:** Language (ISO 639-3 Code)

|              |          |
| ------------ | -------- |
| **Type**     | `string` |
| **Required** | Yes      |

###### <a name="content_tracks_items_clips_items_oneOf_i1_notes_items_phonemes_edited_items_start"></a>1.4.1.1.1.2.3.1.6.1.1.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > phonemes > edited > Phoneme > start`

**Title:** Start Position (Milliseconds from Note On)

|              |           |
| ------------ | --------- |
| **Type**     | `integer` |
| **Required** | Yes       |

| Restrictions |                  |
| ------------ | ---------------- |
| **Minimum**  | &ge; -2147483648 |
| **Maximum**  | &le; 2147483647  |

###### <a name="content_tracks_items_clips_items_oneOf_i1_notes_items_phonemes_edited_items_token"></a>1.4.1.1.1.2.3.1.6.1.1.3. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > phonemes > edited > Phoneme > token`

**Title:** Phoneme Token

|              |          |
| ------------ | -------- |
| **Type**     | `string` |
| **Required** | Yes      |

###### <a name="content_tracks_items_clips_items_oneOf_i1_notes_items_phonemes_edited_items_onset"></a>1.4.1.1.1.2.3.1.6.1.1.4. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > phonemes > edited > Phoneme > onset`

**Title:** Onset Flag

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | Yes       |

###### <a name="content_tracks_items_clips_items_oneOf_i1_notes_items_phonemes_original"></a>1.4.1.1.1.2.3.1.6.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > phonemes > original`

**Title:** Original Phonemes Generated from Pronunciation

|              |         |
| ------------ | ------- |
| **Type**     | `array` |
| **Required** | Yes     |

|                      | Array restrictions |
| -------------------- | ------------------ |
| **Min items**        | N/A                |
| **Max items**        | N/A                |
| **Items unicity**    | False              |
| **Additional items** | False              |
| **Tuple validation** | See below          |

| Each item of this array must be                                                           | Description |
| ----------------------------------------------------------------------------------------- | ----------- |
| [Phoneme](#content_tracks_items_clips_items_oneOf_i1_notes_items_phonemes_original_items) | -           |

###### <a name="content_tracks_items_clips_items_oneOf_i1_notes_items_phonemes_original_items"></a>1.4.1.1.1.2.3.1.6.2.1. DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > phonemes > original > Phoneme

**Title:** Phoneme

|                           |                 |
| ------------------------- | --------------- |
| **Type**                  | `object`        |
| **Required**              | No              |
| **Additional properties** | Not allowed     |
| **Defined in**            | #/$defs/phoneme |

| Property                                                                                               | Pattern | Type    | Deprecated | Definition | Title/Description                          |
| ------------------------------------------------------------------------------------------------------ | ------- | ------- | ---------- | ---------- | ------------------------------------------ |
| + [language](#content_tracks_items_clips_items_oneOf_i1_notes_items_phonemes_original_items_language ) | No      | string  | No         | -          | Language (ISO 639-3 Code)                  |
| + [start](#content_tracks_items_clips_items_oneOf_i1_notes_items_phonemes_original_items_start )       | No      | integer | No         | -          | Start Position (Milliseconds from Note On) |
| + [token](#content_tracks_items_clips_items_oneOf_i1_notes_items_phonemes_original_items_token )       | No      | string  | No         | -          | Phoneme Token                              |
| + [onset](#content_tracks_items_clips_items_oneOf_i1_notes_items_phonemes_original_items_onset )       | No      | boolean | No         | -          | Onset Flag                                 |

###### <a name="content_tracks_items_clips_items_oneOf_i1_notes_items_phonemes_original_items_language"></a>1.4.1.1.1.2.3.1.6.2.1.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > phonemes > original > Phoneme > language`

**Title:** Language (ISO 639-3 Code)

|              |          |
| ------------ | -------- |
| **Type**     | `string` |
| **Required** | Yes      |

###### <a name="content_tracks_items_clips_items_oneOf_i1_notes_items_phonemes_original_items_start"></a>1.4.1.1.1.2.3.1.6.2.1.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > phonemes > original > Phoneme > start`

**Title:** Start Position (Milliseconds from Note On)

|              |           |
| ------------ | --------- |
| **Type**     | `integer` |
| **Required** | Yes       |

| Restrictions |                  |
| ------------ | ---------------- |
| **Minimum**  | &ge; -2147483648 |
| **Maximum**  | &le; 2147483647  |

###### <a name="content_tracks_items_clips_items_oneOf_i1_notes_items_phonemes_original_items_token"></a>1.4.1.1.1.2.3.1.6.2.1.3. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > phonemes > original > Phoneme > token`

**Title:** Phoneme Token

|              |          |
| ------------ | -------- |
| **Type**     | `string` |
| **Required** | Yes      |

###### <a name="content_tracks_items_clips_items_oneOf_i1_notes_items_phonemes_original_items_onset"></a>1.4.1.1.1.2.3.1.6.2.1.4. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > phonemes > original > Phoneme > onset`

**Title:** Onset Flag

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | Yes       |

###### <a name="content_tracks_items_clips_items_oneOf_i1_notes_items_pos"></a>1.4.1.1.1.2.3.1.7. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > pos`

**Title:** Position (Ticks)

|              |           |
| ------------ | --------- |
| **Type**     | `integer` |
| **Required** | Yes       |

| Restrictions |                 |
| ------------ | --------------- |
| **Minimum**  | &ge; 0          |
| **Maximum**  | &le; 2147483647 |

###### <a name="content_tracks_items_clips_items_oneOf_i1_notes_items_pronunciation"></a>1.4.1.1.1.2.3.1.8. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > pronunciation`

**Title:** Pronunciation

|                           |             |
| ------------------------- | ----------- |
| **Type**                  | `object`    |
| **Required**              | Yes         |
| **Additional properties** | Not allowed |

| Property                                                                                     | Pattern | Type   | Deprecated | Definition | Title/Description                       |
| -------------------------------------------------------------------------------------------- | ------- | ------ | ---------- | ---------- | --------------------------------------- |
| + [edited](#content_tracks_items_clips_items_oneOf_i1_notes_items_pronunciation_edited )     | No      | string | No         | -          | Edited Pronunciation                    |
| + [original](#content_tracks_items_clips_items_oneOf_i1_notes_items_pronunciation_original ) | No      | string | No         | -          | Original Pronunciation Generated by G2P |

###### <a name="content_tracks_items_clips_items_oneOf_i1_notes_items_pronunciation_edited"></a>1.4.1.1.1.2.3.1.8.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > pronunciation > edited`

**Title:** Edited Pronunciation

|              |          |
| ------------ | -------- |
| **Type**     | `string` |
| **Required** | Yes      |

###### <a name="content_tracks_items_clips_items_oneOf_i1_notes_items_pronunciation_original"></a>1.4.1.1.1.2.3.1.8.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > pronunciation > original`

**Title:** Original Pronunciation Generated by G2P

|              |          |
| ------------ | -------- |
| **Type**     | `string` |
| **Required** | Yes      |

###### <a name="content_tracks_items_clips_items_oneOf_i1_notes_items_vibrato"></a>1.4.1.1.1.2.3.1.9. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > vibrato`

**Title:** Vibrato

|                           |             |
| ------------------------- | ----------- |
| **Type**                  | `object`    |
| **Required**              | Yes         |
| **Additional properties** | Not allowed |

| Property                                                                           | Pattern | Type    | Deprecated | Definition | Title/Description         |
| ---------------------------------------------------------------------------------- | ------- | ------- | ---------- | ---------- | ------------------------- |
| + [amp](#content_tracks_items_clips_items_oneOf_i1_notes_items_vibrato_amp )       | No      | integer | No         | -          | Amplitude (Cent)          |
| + [end](#content_tracks_items_clips_items_oneOf_i1_notes_items_vibrato_end )       | No      | number  | No         | -          | End (Note Length Ratio)   |
| + [freq](#content_tracks_items_clips_items_oneOf_i1_notes_items_vibrato_freq )     | No      | number  | No         | -          | Frequency (Hz)            |
| + [offset](#content_tracks_items_clips_items_oneOf_i1_notes_items_vibrato_offset ) | No      | integer | No         | -          | Offset of Tune (Cent)     |
| + [phase](#content_tracks_items_clips_items_oneOf_i1_notes_items_vibrato_phase )   | No      | number  | No         | -          | Phase                     |
| + [points](#content_tracks_items_clips_items_oneOf_i1_notes_items_vibrato_points ) | No      | object  | No         | -          | -                         |
| + [start](#content_tracks_items_clips_items_oneOf_i1_notes_items_vibrato_start )   | No      | number  | No         | -          | Start (Note Length Ratio) |

###### <a name="content_tracks_items_clips_items_oneOf_i1_notes_items_vibrato_amp"></a>1.4.1.1.1.2.3.1.9.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > vibrato > amp`

**Title:** Amplitude (Cent)

|              |           |
| ------------ | --------- |
| **Type**     | `integer` |
| **Required** | Yes       |

| Restrictions |                 |
| ------------ | --------------- |
| **Minimum**  | &ge; 0          |
| **Maximum**  | &le; 2147483647 |

###### <a name="content_tracks_items_clips_items_oneOf_i1_notes_items_vibrato_end"></a>1.4.1.1.1.2.3.1.9.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > vibrato > end`

**Title:** End (Note Length Ratio)

|              |          |
| ------------ | -------- |
| **Type**     | `number` |
| **Required** | Yes      |

| Restrictions |        |
| ------------ | ------ |
| **Minimum**  | &ge; 0 |
| **Maximum**  | &le; 1 |

###### <a name="content_tracks_items_clips_items_oneOf_i1_notes_items_vibrato_freq"></a>1.4.1.1.1.2.3.1.9.3. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > vibrato > freq`

**Title:** Frequency (Hz)

|              |          |
| ------------ | -------- |
| **Type**     | `number` |
| **Required** | Yes      |

| Restrictions |        |
| ------------ | ------ |
| **Minimum**  | &ge; 0 |

###### <a name="content_tracks_items_clips_items_oneOf_i1_notes_items_vibrato_offset"></a>1.4.1.1.1.2.3.1.9.4. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > vibrato > offset`

**Title:** Offset of Tune (Cent)

|              |           |
| ------------ | --------- |
| **Type**     | `integer` |
| **Required** | Yes       |

| Restrictions |                  |
| ------------ | ---------------- |
| **Minimum**  | &ge; -2147483648 |
| **Maximum**  | &le; 2147483647  |

###### <a name="content_tracks_items_clips_items_oneOf_i1_notes_items_vibrato_phase"></a>1.4.1.1.1.2.3.1.9.5. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > vibrato > phase`

**Title:** Phase

|              |          |
| ------------ | -------- |
| **Type**     | `number` |
| **Required** | Yes      |

| Restrictions |        |
| ------------ | ------ |
| **Minimum**  | &ge; 0 |
| **Maximum**  | &le; 1 |

###### <a name="content_tracks_items_clips_items_oneOf_i1_notes_items_vibrato_points"></a>1.4.1.1.1.2.3.1.9.6. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > vibrato > points`

|                           |             |
| ------------------------- | ----------- |
| **Type**                  | `object`    |
| **Required**              | Yes         |
| **Additional properties** | Not allowed |

| Property                                                                              | Pattern | Type            | Deprecated | Definition               | Title/Description |
| ------------------------------------------------------------------------------------- | ------- | --------------- | ---------- | ------------------------ | ----------------- |
| + [amp](#content_tracks_items_clips_items_oneOf_i1_notes_items_vibrato_points_amp )   | No      | array of object | No         | In #/$defs/controlPoints | Control Points    |
| + [freq](#content_tracks_items_clips_items_oneOf_i1_notes_items_vibrato_points_freq ) | No      | array of object | No         | In #/$defs/controlPoints | Control Points    |

###### <a name="content_tracks_items_clips_items_oneOf_i1_notes_items_vibrato_points_amp"></a>1.4.1.1.1.2.3.1.9.6.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > vibrato > points > amp`

**Title:** Control Points

|                |                       |
| -------------- | --------------------- |
| **Type**       | `array of object`     |
| **Required**   | Yes                   |
| **Defined in** | #/$defs/controlPoints |

|                      | Array restrictions |
| -------------------- | ------------------ |
| **Min items**        | N/A                |
| **Max items**        | N/A                |
| **Items unicity**    | False              |
| **Additional items** | False              |
| **Tuple validation** | See below          |

| Each item of this array must be                                                                  | Description |
| ------------------------------------------------------------------------------------------------ | ----------- |
| [Control Point](#content_tracks_items_clips_items_oneOf_i1_notes_items_vibrato_points_amp_items) | -           |

###### <a name="content_tracks_items_clips_items_oneOf_i1_notes_items_vibrato_points_amp_items"></a>1.4.1.1.1.2.3.1.9.6.1.1. DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > vibrato > points > amp > Control Point

**Title:** Control Point

|                           |             |
| ------------------------- | ----------- |
| **Type**                  | `object`    |
| **Required**              | No          |
| **Additional properties** | Not allowed |

| Property                                                                                  | Pattern | Type   | Deprecated | Definition | Title/Description              |
| ----------------------------------------------------------------------------------------- | ------- | ------ | ---------- | ---------- | ------------------------------ |
| + [x](#content_tracks_items_clips_items_oneOf_i1_notes_items_vibrato_points_amp_items_x ) | No      | number | No         | -          | X Position (Note Length Ratio) |
| + [y](#content_tracks_items_clips_items_oneOf_i1_notes_items_vibrato_points_amp_items_y ) | No      | number | No         | -          | Y Position (Ratio)             |

###### <a name="content_tracks_items_clips_items_oneOf_i1_notes_items_vibrato_points_amp_items_x"></a>1.4.1.1.1.2.3.1.9.6.1.1.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > vibrato > points > amp > Control Point > x`

**Title:** X Position (Note Length Ratio)

|              |          |
| ------------ | -------- |
| **Type**     | `number` |
| **Required** | Yes      |

###### <a name="content_tracks_items_clips_items_oneOf_i1_notes_items_vibrato_points_amp_items_y"></a>1.4.1.1.1.2.3.1.9.6.1.1.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > vibrato > points > amp > Control Point > y`

**Title:** Y Position (Ratio)

|              |          |
| ------------ | -------- |
| **Type**     | `number` |
| **Required** | Yes      |

###### <a name="content_tracks_items_clips_items_oneOf_i1_notes_items_vibrato_points_freq"></a>1.4.1.1.1.2.3.1.9.6.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > vibrato > points > freq`

**Title:** Control Points

|                |                       |
| -------------- | --------------------- |
| **Type**       | `array of object`     |
| **Required**   | Yes                   |
| **Defined in** | #/$defs/controlPoints |

|                      | Array restrictions |
| -------------------- | ------------------ |
| **Min items**        | N/A                |
| **Max items**        | N/A                |
| **Items unicity**    | False              |
| **Additional items** | False              |
| **Tuple validation** | See below          |

| Each item of this array must be                                                                   | Description |
| ------------------------------------------------------------------------------------------------- | ----------- |
| [Control Point](#content_tracks_items_clips_items_oneOf_i1_notes_items_vibrato_points_freq_items) | -           |

###### <a name="content_tracks_items_clips_items_oneOf_i1_notes_items_vibrato_points_freq_items"></a>1.4.1.1.1.2.3.1.9.6.2.1. DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > vibrato > points > freq > Control Point

**Title:** Control Point

|                           |             |
| ------------------------- | ----------- |
| **Type**                  | `object`    |
| **Required**              | No          |
| **Additional properties** | Not allowed |

| Property                                                                                   | Pattern | Type   | Deprecated | Definition | Title/Description              |
| ------------------------------------------------------------------------------------------ | ------- | ------ | ---------- | ---------- | ------------------------------ |
| + [x](#content_tracks_items_clips_items_oneOf_i1_notes_items_vibrato_points_freq_items_x ) | No      | number | No         | -          | X Position (Note Length Ratio) |
| + [y](#content_tracks_items_clips_items_oneOf_i1_notes_items_vibrato_points_freq_items_y ) | No      | number | No         | -          | Y Position (Ratio)             |

###### <a name="content_tracks_items_clips_items_oneOf_i1_notes_items_vibrato_points_freq_items_x"></a>1.4.1.1.1.2.3.1.9.6.2.1.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > vibrato > points > freq > Control Point > x`

**Title:** X Position (Note Length Ratio)

|              |          |
| ------------ | -------- |
| **Type**     | `number` |
| **Required** | Yes      |

###### <a name="content_tracks_items_clips_items_oneOf_i1_notes_items_vibrato_points_freq_items_y"></a>1.4.1.1.1.2.3.1.9.6.2.1.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > vibrato > points > freq > Control Point > y`

**Title:** Y Position (Ratio)

|              |          |
| ------------ | -------- |
| **Type**     | `number` |
| **Required** | Yes      |

###### <a name="content_tracks_items_clips_items_oneOf_i1_notes_items_vibrato_start"></a>1.4.1.1.1.2.3.1.9.7. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > vibrato > start`

**Title:** Start (Note Length Ratio)

|              |          |
| ------------ | -------- |
| **Type**     | `number` |
| **Required** | Yes      |

| Restrictions |        |
| ------------ | ------ |
| **Minimum**  | &ge; 0 |
| **Maximum**  | &le; 1 |

###### <a name="content_tracks_items_clips_items_oneOf_i1_notes_items_workspace"></a>1.4.1.1.1.2.3.1.10. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > workspace`

**Title:** Workspace

|                           |                                                                                                                                              |
| ------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
| **Type**                  | `object`                                                                                                                                     |
| **Required**              | Yes                                                                                                                                          |
| **Additional properties** | [Each additional property must conform to the schema](#content_tracks_items_clips_items_oneOf_i1_notes_items_workspace_additionalProperties) |
| **Defined in**            | #/$defs/workspace                                                                                                                            |

**Description:** A flexible object for storing application-specific data.

| Property                                                                                     | Pattern | Type   | Deprecated | Definition | Title/Description |
| -------------------------------------------------------------------------------------------- | ------- | ------ | ---------- | ---------- | ----------------- |
| - [](#content_tracks_items_clips_items_oneOf_i1_notes_items_workspace_additionalProperties ) | No      | object | No         | -          | Workspace Item    |

###### <a name="content_tracks_items_clips_items_oneOf_i1_notes_items_workspace_additionalProperties"></a>1.4.1.1.1.2.3.1.10.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > notes > Note > workspace > Workspace Item`

**Title:** Workspace Item

|                           |                  |
| ------------------------- | ---------------- |
| **Type**                  | `object`         |
| **Required**              | No               |
| **Additional properties** | Any type allowed |

###### <a name="content_tracks_items_clips_items_oneOf_i1_params"></a>1.4.1.1.1.2.4. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params`

**Title:** Parameters

|                           |                                                                                                                               |
| ------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| **Type**                  | `object`                                                                                                                      |
| **Required**              | Yes                                                                                                                           |
| **Additional properties** | [Each additional property must conform to the schema](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties) |

| Property                                                                      | Pattern | Type   | Deprecated | Definition       | Title/Description |
| ----------------------------------------------------------------------------- | ------- | ------ | ---------- | ---------------- | ----------------- |
| - [](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties ) | No      | object | No         | In #/$defs/param | Parameter         |

###### <a name="content_tracks_items_clips_items_oneOf_i1_params_additionalProperties"></a>1.4.1.1.1.2.4.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter`

**Title:** Parameter

|                           |               |
| ------------------------- | ------------- |
| **Type**                  | `object`      |
| **Required**              | No            |
| **Additional properties** | Not allowed   |
| **Defined in**            | #/$defs/param |

| Property                                                                                         | Pattern | Type  | Deprecated | Definition                | Title/Description          |
| ------------------------------------------------------------------------------------------------ | ------- | ----- | ---------- | ------------------------- | -------------------------- |
| + [edited](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_edited )       | No      | array | No         | In #/$defs/paramCurveList | Edited Parameter Curves    |
| + [transform](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_transform ) | No      | array | No         | In #/$defs/paramCurveList | Transform Parameter Curves |
| + [original](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_original )   | No      | array | No         | In #/$defs/paramCurveList | Original Parameter Curves  |

###### <a name="content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_edited"></a>1.4.1.1.1.2.4.1.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > edited`

**Title:** Edited Parameter Curves

|                |                        |
| -------------- | ---------------------- |
| **Type**       | `array`                |
| **Required**   | Yes                    |
| **Defined in** | #/$defs/paramCurveList |

|                      | Array restrictions |
| -------------------- | ------------------ |
| **Min items**        | N/A                |
| **Max items**        | N/A                |
| **Items unicity**    | False              |
| **Additional items** | False              |
| **Tuple validation** | See below          |

| Each item of this array must be                                                                        | Description |
| ------------------------------------------------------------------------------------------------------ | ----------- |
| [Parameter Curve](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_edited_items) | -           |

###### <a name="content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_edited_items"></a>1.4.1.1.1.2.4.1.1.1. DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > edited > Parameter Curve

**Title:** Parameter Curve

|                           |                    |
| ------------------------- | ------------------ |
| **Type**                  | `combining`        |
| **Required**              | No                 |
| **Additional properties** | Any type allowed   |
| **Defined in**            | #/$defs/paramCurve |

| One of(Option)                                                                                                         |
| ---------------------------------------------------------------------------------------------------------------------- |
| [Anchor Parameter Curve](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_edited_items_oneOf_i0) |
| [Free Parameter Curve](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_edited_items_oneOf_i1)   |

###### <a name="content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_edited_items_oneOf_i0"></a>1.4.1.1.1.2.4.1.1.1.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > edited > Parameter Curve > oneOf > Anchor Parameter Curve`

**Title:** Anchor Parameter Curve

|                           |                          |
| ------------------------- | ------------------------ |
| **Type**                  | `object`                 |
| **Required**              | No                       |
| **Additional properties** | Not allowed              |
| **Defined in**            | #/$defs/paramCurveAnchor |

| Property                                                                                                       | Pattern | Type            | Deprecated | Definition | Title/Description      |
| -------------------------------------------------------------------------------------------------------------- | ------- | --------------- | ---------- | ---------- | ---------------------- |
| + [nodes](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_edited_items_oneOf_i0_nodes ) | No      | array of object | No         | -          | Anchor Node List       |
| + [start](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_edited_items_oneOf_i0_start ) | No      | integer         | No         | -          | Start Position (Ticks) |
| + [type](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_edited_items_oneOf_i0_type )   | No      | const           | No         | -          | Curve Type             |

###### <a name="content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_edited_items_oneOf_i0_nodes"></a>1.4.1.1.1.2.4.1.1.1.1.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > edited > Parameter Curve > oneOf > Anchor Parameter Curve > nodes`

**Title:** Anchor Node List

|              |                   |
| ------------ | ----------------- |
| **Type**     | `array of object` |
| **Required** | Yes               |

|                      | Array restrictions |
| -------------------- | ------------------ |
| **Min items**        | N/A                |
| **Max items**        | N/A                |
| **Items unicity**    | False              |
| **Additional items** | False              |
| **Tuple validation** | See below          |

| Each item of this array must be                                                                                         | Description |
| ----------------------------------------------------------------------------------------------------------------------- | ----------- |
| [Anchor Node](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_edited_items_oneOf_i0_nodes_items) | -           |

###### <a name="content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_edited_items_oneOf_i0_nodes_items"></a>1.4.1.1.1.2.4.1.1.1.1.1.1. DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > edited > Parameter Curve > oneOf > Anchor Parameter Curve > nodes > Anchor Node

**Title:** Anchor Node

|                           |             |
| ------------------------- | ----------- |
| **Type**                  | `object`    |
| **Required**              | No          |
| **Additional properties** | Not allowed |

| Property                                                                                                                     | Pattern | Type             | Deprecated | Definition | Title/Description            |
| ---------------------------------------------------------------------------------------------------------------------------- | ------- | ---------------- | ---------- | ---------- | ---------------------------- |
| + [interp](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_edited_items_oneOf_i0_nodes_items_interp ) | No      | enum (of string) | No         | -          | Interpolation Type           |
| + [x](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_edited_items_oneOf_i0_nodes_items_x )           | No      | integer          | No         | -          | X Position (Ticks)           |
| + [y](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_edited_items_oneOf_i0_nodes_items_y )           | No      | integer          | No         | -          | Y Position (Parameter Value) |

###### <a name="content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_edited_items_oneOf_i0_nodes_items_interp"></a>1.4.1.1.1.2.4.1.1.1.1.1.1.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > edited > Parameter Curve > oneOf > Anchor Parameter Curve > nodes > Anchor Node > interp`

**Title:** Interpolation Type

|              |                    |
| ------------ | ------------------ |
| **Type**     | `enum (of string)` |
| **Required** | Yes                |

Must be one of:
* "none"
* "linear"
* "hermite"

###### <a name="content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_edited_items_oneOf_i0_nodes_items_x"></a>1.4.1.1.1.2.4.1.1.1.1.1.1.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > edited > Parameter Curve > oneOf > Anchor Parameter Curve > nodes > Anchor Node > x`

**Title:** X Position (Ticks)

|              |           |
| ------------ | --------- |
| **Type**     | `integer` |
| **Required** | Yes       |

| Restrictions |                 |
| ------------ | --------------- |
| **Minimum**  | &ge; 0          |
| **Maximum**  | &le; 2147483647 |

###### <a name="content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_edited_items_oneOf_i0_nodes_items_y"></a>1.4.1.1.1.2.4.1.1.1.1.1.1.3. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > edited > Parameter Curve > oneOf > Anchor Parameter Curve > nodes > Anchor Node > y`

**Title:** Y Position (Parameter Value)

|              |           |
| ------------ | --------- |
| **Type**     | `integer` |
| **Required** | Yes       |

| Restrictions |                  |
| ------------ | ---------------- |
| **Minimum**  | &ge; -2147483648 |
| **Maximum**  | &le; 2147483647  |

###### <a name="content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_edited_items_oneOf_i0_start"></a>1.4.1.1.1.2.4.1.1.1.1.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > edited > Parameter Curve > oneOf > Anchor Parameter Curve > start`

**Title:** Start Position (Ticks)

|              |           |
| ------------ | --------- |
| **Type**     | `integer` |
| **Required** | Yes       |

| Restrictions |                  |
| ------------ | ---------------- |
| **Minimum**  | &ge; -2147483648 |
| **Maximum**  | &le; 2147483647  |

###### <a name="content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_edited_items_oneOf_i0_type"></a>1.4.1.1.1.2.4.1.1.1.1.3. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > edited > Parameter Curve > oneOf > Anchor Parameter Curve > type`

**Title:** Curve Type

|              |         |
| ------------ | ------- |
| **Type**     | `const` |
| **Required** | Yes     |

Specific value: `"anchor"`

###### <a name="content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_edited_items_oneOf_i1"></a>1.4.1.1.1.2.4.1.1.1.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > edited > Parameter Curve > oneOf > Free Parameter Curve`

**Title:** Free Parameter Curve

|                           |                        |
| ------------------------- | ---------------------- |
| **Type**                  | `object`               |
| **Required**              | No                     |
| **Additional properties** | Not allowed            |
| **Defined in**            | #/$defs/paramCurveFree |

| Property                                                                                                         | Pattern | Type             | Deprecated | Definition | Title/Description      |
| ---------------------------------------------------------------------------------------------------------------- | ------- | ---------------- | ---------- | ---------- | ---------------------- |
| + [start](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_edited_items_oneOf_i1_start )   | No      | integer          | No         | -          | Start Position (Ticks) |
| + [step](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_edited_items_oneOf_i1_step )     | No      | const            | No         | -          | Step (Ticks)           |
| + [type](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_edited_items_oneOf_i1_type )     | No      | const            | No         | -          | Curve Type             |
| + [values](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_edited_items_oneOf_i1_values ) | No      | array of integer | No         | -          | Value List             |

###### <a name="content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_edited_items_oneOf_i1_start"></a>1.4.1.1.1.2.4.1.1.1.2.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > edited > Parameter Curve > oneOf > Free Parameter Curve > start`

**Title:** Start Position (Ticks)

|              |           |
| ------------ | --------- |
| **Type**     | `integer` |
| **Required** | Yes       |

| Restrictions |                  |
| ------------ | ---------------- |
| **Minimum**  | &ge; -2147483648 |
| **Maximum**  | &le; 2147483647  |

###### <a name="content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_edited_items_oneOf_i1_step"></a>1.4.1.1.1.2.4.1.1.1.2.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > edited > Parameter Curve > oneOf > Free Parameter Curve > step`

**Title:** Step (Ticks)

|              |         |
| ------------ | ------- |
| **Type**     | `const` |
| **Required** | Yes     |

Specific value: `5`

###### <a name="content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_edited_items_oneOf_i1_type"></a>1.4.1.1.1.2.4.1.1.1.2.3. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > edited > Parameter Curve > oneOf > Free Parameter Curve > type`

**Title:** Curve Type

|              |         |
| ------------ | ------- |
| **Type**     | `const` |
| **Required** | Yes     |

Specific value: `"free"`

###### <a name="content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_edited_items_oneOf_i1_values"></a>1.4.1.1.1.2.4.1.1.1.2.4. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > edited > Parameter Curve > oneOf > Free Parameter Curve > values`

**Title:** Value List

|              |                    |
| ------------ | ------------------ |
| **Type**     | `array of integer` |
| **Required** | Yes                |

|                      | Array restrictions |
| -------------------- | ------------------ |
| **Min items**        | N/A                |
| **Max items**        | N/A                |
| **Items unicity**    | False              |
| **Additional items** | False              |
| **Tuple validation** | See below          |

| Each item of this array must be                                                                                              | Description |
| ---------------------------------------------------------------------------------------------------------------------------- | ----------- |
| [Parameter Value](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_edited_items_oneOf_i1_values_items) | -           |

###### <a name="content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_edited_items_oneOf_i1_values_items"></a>1.4.1.1.1.2.4.1.1.1.2.4.1. DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > edited > Parameter Curve > oneOf > Free Parameter Curve > values > Parameter Value

**Title:** Parameter Value

|              |           |
| ------------ | --------- |
| **Type**     | `integer` |
| **Required** | No        |

| Restrictions |                  |
| ------------ | ---------------- |
| **Minimum**  | &ge; -2147483648 |
| **Maximum**  | &le; 2147483647  |

###### <a name="content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_transform"></a>1.4.1.1.1.2.4.1.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > transform`

**Title:** Transform Parameter Curves

|                |                        |
| -------------- | ---------------------- |
| **Type**       | `array`                |
| **Required**   | Yes                    |
| **Defined in** | #/$defs/paramCurveList |

|                      | Array restrictions |
| -------------------- | ------------------ |
| **Min items**        | N/A                |
| **Max items**        | N/A                |
| **Items unicity**    | False              |
| **Additional items** | False              |
| **Tuple validation** | See below          |

| Each item of this array must be                                                                           | Description |
| --------------------------------------------------------------------------------------------------------- | ----------- |
| [Parameter Curve](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_transform_items) | -           |

###### <a name="content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_transform_items"></a>1.4.1.1.1.2.4.1.2.1. DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > transform > Parameter Curve

**Title:** Parameter Curve

|                           |                    |
| ------------------------- | ------------------ |
| **Type**                  | `combining`        |
| **Required**              | No                 |
| **Additional properties** | Any type allowed   |
| **Defined in**            | #/$defs/paramCurve |

| One of(Option)                                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------- |
| [Anchor Parameter Curve](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_transform_items_oneOf_i0) |
| [Free Parameter Curve](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_transform_items_oneOf_i1)   |

###### <a name="content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_transform_items_oneOf_i0"></a>1.4.1.1.1.2.4.1.2.1.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > transform > Parameter Curve > oneOf > Anchor Parameter Curve`

**Title:** Anchor Parameter Curve

|                           |                          |
| ------------------------- | ------------------------ |
| **Type**                  | `object`                 |
| **Required**              | No                       |
| **Additional properties** | Not allowed              |
| **Defined in**            | #/$defs/paramCurveAnchor |

| Property                                                                                                          | Pattern | Type            | Deprecated | Definition | Title/Description      |
| ----------------------------------------------------------------------------------------------------------------- | ------- | --------------- | ---------- | ---------- | ---------------------- |
| + [nodes](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_transform_items_oneOf_i0_nodes ) | No      | array of object | No         | -          | Anchor Node List       |
| + [start](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_transform_items_oneOf_i0_start ) | No      | integer         | No         | -          | Start Position (Ticks) |
| + [type](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_transform_items_oneOf_i0_type )   | No      | const           | No         | -          | Curve Type             |

###### <a name="content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_transform_items_oneOf_i0_nodes"></a>1.4.1.1.1.2.4.1.2.1.1.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > transform > Parameter Curve > oneOf > Anchor Parameter Curve > nodes`

**Title:** Anchor Node List

|              |                   |
| ------------ | ----------------- |
| **Type**     | `array of object` |
| **Required** | Yes               |

|                      | Array restrictions |
| -------------------- | ------------------ |
| **Min items**        | N/A                |
| **Max items**        | N/A                |
| **Items unicity**    | False              |
| **Additional items** | False              |
| **Tuple validation** | See below          |

| Each item of this array must be                                                                                            | Description |
| -------------------------------------------------------------------------------------------------------------------------- | ----------- |
| [Anchor Node](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_transform_items_oneOf_i0_nodes_items) | -           |

###### <a name="content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_transform_items_oneOf_i0_nodes_items"></a>1.4.1.1.1.2.4.1.2.1.1.1.1. DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > transform > Parameter Curve > oneOf > Anchor Parameter Curve > nodes > Anchor Node

**Title:** Anchor Node

|                           |             |
| ------------------------- | ----------- |
| **Type**                  | `object`    |
| **Required**              | No          |
| **Additional properties** | Not allowed |

| Property                                                                                                                        | Pattern | Type             | Deprecated | Definition | Title/Description            |
| ------------------------------------------------------------------------------------------------------------------------------- | ------- | ---------------- | ---------- | ---------- | ---------------------------- |
| + [interp](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_transform_items_oneOf_i0_nodes_items_interp ) | No      | enum (of string) | No         | -          | Interpolation Type           |
| + [x](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_transform_items_oneOf_i0_nodes_items_x )           | No      | integer          | No         | -          | X Position (Ticks)           |
| + [y](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_transform_items_oneOf_i0_nodes_items_y )           | No      | integer          | No         | -          | Y Position (Parameter Value) |

###### <a name="content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_transform_items_oneOf_i0_nodes_items_interp"></a>1.4.1.1.1.2.4.1.2.1.1.1.1.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > transform > Parameter Curve > oneOf > Anchor Parameter Curve > nodes > Anchor Node > interp`

**Title:** Interpolation Type

|              |                    |
| ------------ | ------------------ |
| **Type**     | `enum (of string)` |
| **Required** | Yes                |

Must be one of:
* "none"
* "linear"
* "hermite"

###### <a name="content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_transform_items_oneOf_i0_nodes_items_x"></a>1.4.1.1.1.2.4.1.2.1.1.1.1.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > transform > Parameter Curve > oneOf > Anchor Parameter Curve > nodes > Anchor Node > x`

**Title:** X Position (Ticks)

|              |           |
| ------------ | --------- |
| **Type**     | `integer` |
| **Required** | Yes       |

| Restrictions |                 |
| ------------ | --------------- |
| **Minimum**  | &ge; 0          |
| **Maximum**  | &le; 2147483647 |

###### <a name="content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_transform_items_oneOf_i0_nodes_items_y"></a>1.4.1.1.1.2.4.1.2.1.1.1.1.3. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > transform > Parameter Curve > oneOf > Anchor Parameter Curve > nodes > Anchor Node > y`

**Title:** Y Position (Parameter Value)

|              |           |
| ------------ | --------- |
| **Type**     | `integer` |
| **Required** | Yes       |

| Restrictions |                  |
| ------------ | ---------------- |
| **Minimum**  | &ge; -2147483648 |
| **Maximum**  | &le; 2147483647  |

###### <a name="content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_transform_items_oneOf_i0_start"></a>1.4.1.1.1.2.4.1.2.1.1.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > transform > Parameter Curve > oneOf > Anchor Parameter Curve > start`

**Title:** Start Position (Ticks)

|              |           |
| ------------ | --------- |
| **Type**     | `integer` |
| **Required** | Yes       |

| Restrictions |                  |
| ------------ | ---------------- |
| **Minimum**  | &ge; -2147483648 |
| **Maximum**  | &le; 2147483647  |

###### <a name="content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_transform_items_oneOf_i0_type"></a>1.4.1.1.1.2.4.1.2.1.1.3. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > transform > Parameter Curve > oneOf > Anchor Parameter Curve > type`

**Title:** Curve Type

|              |         |
| ------------ | ------- |
| **Type**     | `const` |
| **Required** | Yes     |

Specific value: `"anchor"`

###### <a name="content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_transform_items_oneOf_i1"></a>1.4.1.1.1.2.4.1.2.1.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > transform > Parameter Curve > oneOf > Free Parameter Curve`

**Title:** Free Parameter Curve

|                           |                        |
| ------------------------- | ---------------------- |
| **Type**                  | `object`               |
| **Required**              | No                     |
| **Additional properties** | Not allowed            |
| **Defined in**            | #/$defs/paramCurveFree |

| Property                                                                                                            | Pattern | Type             | Deprecated | Definition | Title/Description      |
| ------------------------------------------------------------------------------------------------------------------- | ------- | ---------------- | ---------- | ---------- | ---------------------- |
| + [start](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_transform_items_oneOf_i1_start )   | No      | integer          | No         | -          | Start Position (Ticks) |
| + [step](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_transform_items_oneOf_i1_step )     | No      | const            | No         | -          | Step (Ticks)           |
| + [type](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_transform_items_oneOf_i1_type )     | No      | const            | No         | -          | Curve Type             |
| + [values](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_transform_items_oneOf_i1_values ) | No      | array of integer | No         | -          | Value List             |

###### <a name="content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_transform_items_oneOf_i1_start"></a>1.4.1.1.1.2.4.1.2.1.2.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > transform > Parameter Curve > oneOf > Free Parameter Curve > start`

**Title:** Start Position (Ticks)

|              |           |
| ------------ | --------- |
| **Type**     | `integer` |
| **Required** | Yes       |

| Restrictions |                  |
| ------------ | ---------------- |
| **Minimum**  | &ge; -2147483648 |
| **Maximum**  | &le; 2147483647  |

###### <a name="content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_transform_items_oneOf_i1_step"></a>1.4.1.1.1.2.4.1.2.1.2.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > transform > Parameter Curve > oneOf > Free Parameter Curve > step`

**Title:** Step (Ticks)

|              |         |
| ------------ | ------- |
| **Type**     | `const` |
| **Required** | Yes     |

Specific value: `5`

###### <a name="content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_transform_items_oneOf_i1_type"></a>1.4.1.1.1.2.4.1.2.1.2.3. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > transform > Parameter Curve > oneOf > Free Parameter Curve > type`

**Title:** Curve Type

|              |         |
| ------------ | ------- |
| **Type**     | `const` |
| **Required** | Yes     |

Specific value: `"free"`

###### <a name="content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_transform_items_oneOf_i1_values"></a>1.4.1.1.1.2.4.1.2.1.2.4. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > transform > Parameter Curve > oneOf > Free Parameter Curve > values`

**Title:** Value List

|              |                    |
| ------------ | ------------------ |
| **Type**     | `array of integer` |
| **Required** | Yes                |

|                      | Array restrictions |
| -------------------- | ------------------ |
| **Min items**        | N/A                |
| **Max items**        | N/A                |
| **Items unicity**    | False              |
| **Additional items** | False              |
| **Tuple validation** | See below          |

| Each item of this array must be                                                                                                 | Description |
| ------------------------------------------------------------------------------------------------------------------------------- | ----------- |
| [Parameter Value](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_transform_items_oneOf_i1_values_items) | -           |

###### <a name="content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_transform_items_oneOf_i1_values_items"></a>1.4.1.1.1.2.4.1.2.1.2.4.1. DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > transform > Parameter Curve > oneOf > Free Parameter Curve > values > Parameter Value

**Title:** Parameter Value

|              |           |
| ------------ | --------- |
| **Type**     | `integer` |
| **Required** | No        |

| Restrictions |                  |
| ------------ | ---------------- |
| **Minimum**  | &ge; -2147483648 |
| **Maximum**  | &le; 2147483647  |

###### <a name="content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_original"></a>1.4.1.1.1.2.4.1.3. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > original`

**Title:** Original Parameter Curves

|                |                        |
| -------------- | ---------------------- |
| **Type**       | `array`                |
| **Required**   | Yes                    |
| **Defined in** | #/$defs/paramCurveList |

|                      | Array restrictions |
| -------------------- | ------------------ |
| **Min items**        | N/A                |
| **Max items**        | N/A                |
| **Items unicity**    | False              |
| **Additional items** | False              |
| **Tuple validation** | See below          |

| Each item of this array must be                                                                          | Description |
| -------------------------------------------------------------------------------------------------------- | ----------- |
| [Parameter Curve](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_original_items) | -           |

###### <a name="content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_original_items"></a>1.4.1.1.1.2.4.1.3.1. DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > original > Parameter Curve

**Title:** Parameter Curve

|                           |                    |
| ------------------------- | ------------------ |
| **Type**                  | `combining`        |
| **Required**              | No                 |
| **Additional properties** | Any type allowed   |
| **Defined in**            | #/$defs/paramCurve |

| One of(Option)                                                                                                           |
| ------------------------------------------------------------------------------------------------------------------------ |
| [Anchor Parameter Curve](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_original_items_oneOf_i0) |
| [Free Parameter Curve](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_original_items_oneOf_i1)   |

###### <a name="content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_original_items_oneOf_i0"></a>1.4.1.1.1.2.4.1.3.1.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > original > Parameter Curve > oneOf > Anchor Parameter Curve`

**Title:** Anchor Parameter Curve

|                           |                          |
| ------------------------- | ------------------------ |
| **Type**                  | `object`                 |
| **Required**              | No                       |
| **Additional properties** | Not allowed              |
| **Defined in**            | #/$defs/paramCurveAnchor |

| Property                                                                                                         | Pattern | Type            | Deprecated | Definition | Title/Description      |
| ---------------------------------------------------------------------------------------------------------------- | ------- | --------------- | ---------- | ---------- | ---------------------- |
| + [nodes](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_original_items_oneOf_i0_nodes ) | No      | array of object | No         | -          | Anchor Node List       |
| + [start](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_original_items_oneOf_i0_start ) | No      | integer         | No         | -          | Start Position (Ticks) |
| + [type](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_original_items_oneOf_i0_type )   | No      | const           | No         | -          | Curve Type             |

###### <a name="content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_original_items_oneOf_i0_nodes"></a>1.4.1.1.1.2.4.1.3.1.1.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > original > Parameter Curve > oneOf > Anchor Parameter Curve > nodes`

**Title:** Anchor Node List

|              |                   |
| ------------ | ----------------- |
| **Type**     | `array of object` |
| **Required** | Yes               |

|                      | Array restrictions |
| -------------------- | ------------------ |
| **Min items**        | N/A                |
| **Max items**        | N/A                |
| **Items unicity**    | False              |
| **Additional items** | False              |
| **Tuple validation** | See below          |

| Each item of this array must be                                                                                           | Description |
| ------------------------------------------------------------------------------------------------------------------------- | ----------- |
| [Anchor Node](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_original_items_oneOf_i0_nodes_items) | -           |

###### <a name="content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_original_items_oneOf_i0_nodes_items"></a>1.4.1.1.1.2.4.1.3.1.1.1.1. DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > original > Parameter Curve > oneOf > Anchor Parameter Curve > nodes > Anchor Node

**Title:** Anchor Node

|                           |             |
| ------------------------- | ----------- |
| **Type**                  | `object`    |
| **Required**              | No          |
| **Additional properties** | Not allowed |

| Property                                                                                                                       | Pattern | Type             | Deprecated | Definition | Title/Description            |
| ------------------------------------------------------------------------------------------------------------------------------ | ------- | ---------------- | ---------- | ---------- | ---------------------------- |
| + [interp](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_original_items_oneOf_i0_nodes_items_interp ) | No      | enum (of string) | No         | -          | Interpolation Type           |
| + [x](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_original_items_oneOf_i0_nodes_items_x )           | No      | integer          | No         | -          | X Position (Ticks)           |
| + [y](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_original_items_oneOf_i0_nodes_items_y )           | No      | integer          | No         | -          | Y Position (Parameter Value) |

###### <a name="content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_original_items_oneOf_i0_nodes_items_interp"></a>1.4.1.1.1.2.4.1.3.1.1.1.1.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > original > Parameter Curve > oneOf > Anchor Parameter Curve > nodes > Anchor Node > interp`

**Title:** Interpolation Type

|              |                    |
| ------------ | ------------------ |
| **Type**     | `enum (of string)` |
| **Required** | Yes                |

Must be one of:
* "none"
* "linear"
* "hermite"

###### <a name="content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_original_items_oneOf_i0_nodes_items_x"></a>1.4.1.1.1.2.4.1.3.1.1.1.1.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > original > Parameter Curve > oneOf > Anchor Parameter Curve > nodes > Anchor Node > x`

**Title:** X Position (Ticks)

|              |           |
| ------------ | --------- |
| **Type**     | `integer` |
| **Required** | Yes       |

| Restrictions |                 |
| ------------ | --------------- |
| **Minimum**  | &ge; 0          |
| **Maximum**  | &le; 2147483647 |

###### <a name="content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_original_items_oneOf_i0_nodes_items_y"></a>1.4.1.1.1.2.4.1.3.1.1.1.1.3. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > original > Parameter Curve > oneOf > Anchor Parameter Curve > nodes > Anchor Node > y`

**Title:** Y Position (Parameter Value)

|              |           |
| ------------ | --------- |
| **Type**     | `integer` |
| **Required** | Yes       |

| Restrictions |                  |
| ------------ | ---------------- |
| **Minimum**  | &ge; -2147483648 |
| **Maximum**  | &le; 2147483647  |

###### <a name="content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_original_items_oneOf_i0_start"></a>1.4.1.1.1.2.4.1.3.1.1.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > original > Parameter Curve > oneOf > Anchor Parameter Curve > start`

**Title:** Start Position (Ticks)

|              |           |
| ------------ | --------- |
| **Type**     | `integer` |
| **Required** | Yes       |

| Restrictions |                  |
| ------------ | ---------------- |
| **Minimum**  | &ge; -2147483648 |
| **Maximum**  | &le; 2147483647  |

###### <a name="content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_original_items_oneOf_i0_type"></a>1.4.1.1.1.2.4.1.3.1.1.3. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > original > Parameter Curve > oneOf > Anchor Parameter Curve > type`

**Title:** Curve Type

|              |         |
| ------------ | ------- |
| **Type**     | `const` |
| **Required** | Yes     |

Specific value: `"anchor"`

###### <a name="content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_original_items_oneOf_i1"></a>1.4.1.1.1.2.4.1.3.1.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > original > Parameter Curve > oneOf > Free Parameter Curve`

**Title:** Free Parameter Curve

|                           |                        |
| ------------------------- | ---------------------- |
| **Type**                  | `object`               |
| **Required**              | No                     |
| **Additional properties** | Not allowed            |
| **Defined in**            | #/$defs/paramCurveFree |

| Property                                                                                                           | Pattern | Type             | Deprecated | Definition | Title/Description      |
| ------------------------------------------------------------------------------------------------------------------ | ------- | ---------------- | ---------- | ---------- | ---------------------- |
| + [start](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_original_items_oneOf_i1_start )   | No      | integer          | No         | -          | Start Position (Ticks) |
| + [step](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_original_items_oneOf_i1_step )     | No      | const            | No         | -          | Step (Ticks)           |
| + [type](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_original_items_oneOf_i1_type )     | No      | const            | No         | -          | Curve Type             |
| + [values](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_original_items_oneOf_i1_values ) | No      | array of integer | No         | -          | Value List             |

###### <a name="content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_original_items_oneOf_i1_start"></a>1.4.1.1.1.2.4.1.3.1.2.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > original > Parameter Curve > oneOf > Free Parameter Curve > start`

**Title:** Start Position (Ticks)

|              |           |
| ------------ | --------- |
| **Type**     | `integer` |
| **Required** | Yes       |

| Restrictions |                  |
| ------------ | ---------------- |
| **Minimum**  | &ge; -2147483648 |
| **Maximum**  | &le; 2147483647  |

###### <a name="content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_original_items_oneOf_i1_step"></a>1.4.1.1.1.2.4.1.3.1.2.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > original > Parameter Curve > oneOf > Free Parameter Curve > step`

**Title:** Step (Ticks)

|              |         |
| ------------ | ------- |
| **Type**     | `const` |
| **Required** | Yes     |

Specific value: `5`

###### <a name="content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_original_items_oneOf_i1_type"></a>1.4.1.1.1.2.4.1.3.1.2.3. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > original > Parameter Curve > oneOf > Free Parameter Curve > type`

**Title:** Curve Type

|              |         |
| ------------ | ------- |
| **Type**     | `const` |
| **Required** | Yes     |

Specific value: `"free"`

###### <a name="content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_original_items_oneOf_i1_values"></a>1.4.1.1.1.2.4.1.3.1.2.4. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > original > Parameter Curve > oneOf > Free Parameter Curve > values`

**Title:** Value List

|              |                    |
| ------------ | ------------------ |
| **Type**     | `array of integer` |
| **Required** | Yes                |

|                      | Array restrictions |
| -------------------- | ------------------ |
| **Min items**        | N/A                |
| **Max items**        | N/A                |
| **Items unicity**    | False              |
| **Additional items** | False              |
| **Tuple validation** | See below          |

| Each item of this array must be                                                                                                | Description |
| ------------------------------------------------------------------------------------------------------------------------------ | ----------- |
| [Parameter Value](#content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_original_items_oneOf_i1_values_items) | -           |

###### <a name="content_tracks_items_clips_items_oneOf_i1_params_additionalProperties_original_items_oneOf_i1_values_items"></a>1.4.1.1.1.2.4.1.3.1.2.4.1. DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > params > Parameter > original > Parameter Curve > oneOf > Free Parameter Curve > values > Parameter Value

**Title:** Parameter Value

|              |           |
| ------------ | --------- |
| **Type**     | `integer` |
| **Required** | No        |

| Restrictions |                  |
| ------------ | ---------------- |
| **Minimum**  | &ge; -2147483648 |
| **Maximum**  | &le; 2147483647  |

###### <a name="content_tracks_items_clips_items_oneOf_i1_sources"></a>1.4.1.1.1.2.5. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > sources`

**Title:** Sources

|                           |                                                                                                                                |
| ------------------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| **Type**                  | `object`                                                                                                                       |
| **Required**              | Yes                                                                                                                            |
| **Additional properties** | [Each additional property must conform to the schema](#content_tracks_items_clips_items_oneOf_i1_sources_additionalProperties) |

| Property                                                                       | Pattern | Type   | Deprecated | Definition | Title/Description |
| ------------------------------------------------------------------------------ | ------- | ------ | ---------- | ---------- | ----------------- |
| - [](#content_tracks_items_clips_items_oneOf_i1_sources_additionalProperties ) | No      | object | No         | -          | Source            |

###### <a name="content_tracks_items_clips_items_oneOf_i1_sources_additionalProperties"></a>1.4.1.1.1.2.5.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > sources > Source`

**Title:** Source

|                           |                  |
| ------------------------- | ---------------- |
| **Type**                  | `object`         |
| **Required**              | No               |
| **Additional properties** | Any type allowed |

###### <a name="content_tracks_items_clips_items_oneOf_i1_time"></a>1.4.1.1.1.2.6. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > time`

**Title:** Clip Time

|                           |                  |
| ------------------------- | ---------------- |
| **Type**                  | `object`         |
| **Required**              | Yes              |
| **Additional properties** | Not allowed      |
| **Defined in**            | #/$defs/clipTime |

| Property                                                                  | Pattern | Type    | Deprecated | Definition | Title/Description      |
| ------------------------------------------------------------------------- | ------- | ------- | ---------- | ---------- | ---------------------- |
| + [clipLen](#content_tracks_items_clips_items_oneOf_i1_time_clipLen )     | No      | integer | No         | -          | Clipped Length (Ticks) |
| + [clipStart](#content_tracks_items_clips_items_oneOf_i1_time_clipStart ) | No      | integer | No         | -          | Clipped Start (Ticks)  |
| + [length](#content_tracks_items_clips_items_oneOf_i1_time_length )       | No      | integer | No         | -          | Length (Ticks)         |
| + [start](#content_tracks_items_clips_items_oneOf_i1_time_start )         | No      | integer | No         | -          | Start Position (Ticks) |

###### <a name="content_tracks_items_clips_items_oneOf_i1_time_clipLen"></a>1.4.1.1.1.2.6.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > time > clipLen`

**Title:** Clipped Length (Ticks)

|              |           |
| ------------ | --------- |
| **Type**     | `integer` |
| **Required** | Yes       |

**Description:** The clipped length relative to `clipStart`

| Restrictions |                 |
| ------------ | --------------- |
| **Minimum**  | &ge; 0          |
| **Maximum**  | &le; 2147483647 |

###### <a name="content_tracks_items_clips_items_oneOf_i1_time_clipStart"></a>1.4.1.1.1.2.6.2. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > time > clipStart`

**Title:** Clipped Start (Ticks)

|              |           |
| ------------ | --------- |
| **Type**     | `integer` |
| **Required** | Yes       |

**Description:** The clipped length relative to `start`

| Restrictions |                 |
| ------------ | --------------- |
| **Minimum**  | &ge; 0          |
| **Maximum**  | &le; 2147483647 |

###### <a name="content_tracks_items_clips_items_oneOf_i1_time_length"></a>1.4.1.1.1.2.6.3. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > time > length`

**Title:** Length (Ticks)

|              |           |
| ------------ | --------- |
| **Type**     | `integer` |
| **Required** | Yes       |

**Description:** The actual length of the content in the clip

| Restrictions |                 |
| ------------ | --------------- |
| **Minimum**  | &ge; 0          |
| **Maximum**  | &le; 2147483647 |

###### <a name="content_tracks_items_clips_items_oneOf_i1_time_start"></a>1.4.1.1.1.2.6.4. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > time > start`

**Title:** Start Position (Ticks)

|              |           |
| ------------ | --------- |
| **Type**     | `integer` |
| **Required** | Yes       |

**Description:** The start position of the content in the clip in the timeline

| Restrictions |                  |
| ------------ | ---------------- |
| **Minimum**  | &ge; -2147483648 |
| **Maximum**  | &le; 2147483647  |

###### <a name="content_tracks_items_clips_items_oneOf_i1_type"></a>1.4.1.1.1.2.7. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > type`

**Title:** Clip Type

|              |         |
| ------------ | ------- |
| **Type**     | `const` |
| **Required** | Yes     |

Specific value: `"singing"`

###### <a name="content_tracks_items_clips_items_oneOf_i1_workspace"></a>1.4.1.1.1.2.8. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > workspace`

**Title:** Workspace

|                           |                                                                                                                                  |
| ------------------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| **Type**                  | `object`                                                                                                                         |
| **Required**              | Yes                                                                                                                              |
| **Additional properties** | [Each additional property must conform to the schema](#content_tracks_items_clips_items_oneOf_i1_workspace_additionalProperties) |
| **Defined in**            | #/$defs/workspace                                                                                                                |

**Description:** A flexible object for storing application-specific data.

| Property                                                                         | Pattern | Type   | Deprecated | Definition | Title/Description |
| -------------------------------------------------------------------------------- | ------- | ------ | ---------- | ---------- | ----------------- |
| - [](#content_tracks_items_clips_items_oneOf_i1_workspace_additionalProperties ) | No      | object | No         | -          | Workspace Item    |

###### <a name="content_tracks_items_clips_items_oneOf_i1_workspace_additionalProperties"></a>1.4.1.1.1.2.8.1. Property `DiffScope Project Exchange Format > content > tracks > Track > clips > Clip > oneOf > Singing Clip > workspace > Workspace Item`

**Title:** Workspace Item

|                           |                  |
| ------------------------- | ---------------- |
| **Type**                  | `object`         |
| **Required**              | No               |
| **Additional properties** | Any type allowed |

##### <a name="content_tracks_items_control"></a>1.4.1.2. Property `DiffScope Project Exchange Format > content > tracks > Track > control`

**Title:** Track Control

|                           |                      |
| ------------------------- | -------------------- |
| **Type**                  | `object`             |
| **Required**              | Yes                  |
| **Additional properties** | Not allowed          |
| **Defined in**            | #/$defs/trackControl |

| Property                                      | Pattern | Type    | Deprecated | Definition | Title/Description |
| --------------------------------------------- | ------- | ------- | ---------- | ---------- | ----------------- |
| + [gain](#content_tracks_items_control_gain ) | No      | number  | No         | -          | Gain              |
| + [mute](#content_tracks_items_control_mute ) | No      | boolean | No         | -          | Mute              |
| + [pan](#content_tracks_items_control_pan )   | No      | number  | No         | -          | Pan               |
| + [solo](#content_tracks_items_control_solo ) | No      | boolean | No         | -          | Solo              |

###### <a name="content_tracks_items_control_gain"></a>1.4.1.2.1. Property `DiffScope Project Exchange Format > content > tracks > Track > control > gain`

**Title:** Gain

|              |          |
| ------------ | -------- |
| **Type**     | `number` |
| **Required** | Yes      |

###### <a name="content_tracks_items_control_mute"></a>1.4.1.2.2. Property `DiffScope Project Exchange Format > content > tracks > Track > control > mute`

**Title:** Mute

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | Yes       |

###### <a name="content_tracks_items_control_pan"></a>1.4.1.2.3. Property `DiffScope Project Exchange Format > content > tracks > Track > control > pan`

**Title:** Pan

|              |          |
| ------------ | -------- |
| **Type**     | `number` |
| **Required** | Yes      |

| Restrictions |         |
| ------------ | ------- |
| **Minimum**  | &ge; -1 |
| **Maximum**  | &le; 1  |

###### <a name="content_tracks_items_control_solo"></a>1.4.1.2.4. Property `DiffScope Project Exchange Format > content > tracks > Track > control > solo`

**Title:** Solo

|              |           |
| ------------ | --------- |
| **Type**     | `boolean` |
| **Required** | Yes       |

##### <a name="content_tracks_items_name"></a>1.4.1.3. Property `DiffScope Project Exchange Format > content > tracks > Track > name`

**Title:** Track Name

|              |          |
| ------------ | -------- |
| **Type**     | `string` |
| **Required** | Yes      |

##### <a name="content_tracks_items_workspace"></a>1.4.1.4. Property `DiffScope Project Exchange Format > content > tracks > Track > workspace`

**Title:** Workspace

|                           |                                                                                                             |
| ------------------------- | ----------------------------------------------------------------------------------------------------------- |
| **Type**                  | `object`                                                                                                    |
| **Required**              | Yes                                                                                                         |
| **Additional properties** | [Each additional property must conform to the schema](#content_tracks_items_workspace_additionalProperties) |
| **Defined in**            | #/$defs/workspace                                                                                           |

**Description:** A flexible object for storing application-specific data.

| Property                                                    | Pattern | Type   | Deprecated | Definition | Title/Description |
| ----------------------------------------------------------- | ------- | ------ | ---------- | ---------- | ----------------- |
| - [](#content_tracks_items_workspace_additionalProperties ) | No      | object | No         | -          | Workspace Item    |

###### <a name="content_tracks_items_workspace_additionalProperties"></a>1.4.1.4.1. Property `DiffScope Project Exchange Format > content > tracks > Track > workspace > Workspace Item`

**Title:** Workspace Item

|                           |                  |
| ------------------------- | ---------------- |
| **Type**                  | `object`         |
| **Required**              | No               |
| **Additional properties** | Any type allowed |

### <a name="content_workspace"></a>1.5. Property `DiffScope Project Exchange Format > content > workspace`

**Title:** Workspace

|                           |                                                                                                |
| ------------------------- | ---------------------------------------------------------------------------------------------- |
| **Type**                  | `object`                                                                                       |
| **Required**              | Yes                                                                                            |
| **Additional properties** | [Each additional property must conform to the schema](#content_workspace_additionalProperties) |
| **Defined in**            | #/$defs/workspace                                                                              |

**Description:** A flexible object for storing application-specific data.

| Property                                       | Pattern | Type   | Deprecated | Definition | Title/Description |
| ---------------------------------------------- | ------- | ------ | ---------- | ---------- | ----------------- |
| - [](#content_workspace_additionalProperties ) | No      | object | No         | -          | Workspace Item    |

#### <a name="content_workspace_additionalProperties"></a>1.5.1. Property `DiffScope Project Exchange Format > content > workspace > Workspace Item`

**Title:** Workspace Item

|                           |                  |
| ------------------------- | ---------------- |
| **Type**                  | `object`         |
| **Required**              | No               |
| **Additional properties** | Any type allowed |

## <a name="version"></a>2. Property `DiffScope Project Exchange Format > version`

**Title:** Version

|              |         |
| ------------ | ------- |
| **Type**     | `const` |
| **Required** | Yes     |

Specific value: `"1.0.0"`

----------------------------------------------------------------------------------------------------------------------------
