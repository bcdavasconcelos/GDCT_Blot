tags: automação, macOS

# Karabiner  
  
  
O [Karabiner](https://pqrs.org/osx/karabiner/) é um aplicativo gratuito de código aberto para customizar o teclado no macOS. Ele pode ser utilizado para re-mapear teclas com pouco uso, como `CAPS LOCK` ou `⌥-Direita`, e transformá-las em algo mais útil, como a combinação ⇧⌃⌥⌘, abrindo inúmeras possibilidades de criar novos atalhos. No meu sistema, por exemplo, `⌥ ←` (=`⇧⌃⌥⌘←`) ativa um macro do Keyboard Maestro que move o aplicativo em primeiro plano para a metade esquerda da tela.  
  
Similarmente…  
- `⌥ →` (=`⇧⌃⌥⌘→`) move para a metade direita.  
- `⌥ ↑` (=`⇧⌃⌥⌘↑`) move para a metade superior.  
- `⌥ ↓` (=`⇧⌃⌥⌘↓`) move para a metade inferior.  
  
A tecla `CAPS LOCK`, por sua vez, tornou-se `F20`, que é um atalho para um macro que muda o teclado (pt_BR ⇆ GRC) e ativa o perfil correspondente do Karabiner (você pode criar inúmeros perfis). No perfil para o Grego, transformei a letra `u` em `υ`, `y` em `;` e `q` em `θ`. Por algum motivo sempre me incomodou o `υ` ficar na tecla `y`.  
  
  
## Configurando  
  
Para configurar o Karabiner, você pode utilizar a interface do próprio software, ou editar o arquivo JSON. Se quiser experimentar esse último método, abra o terminal e dê o seguinte comando:  
  
```  
open ~/.config/karabiner/karabiner.json  
```  
  
Ou você pode abrir o finder, pressionar `⇧⌘G`, colar `~/.config/karabiner/karabiner.json` e pressionar `enter`.  
  
Abaixo transcrevo as minhas configurações. Se você copiar e colar o código terá exatamente as mesmas configurações e funções.  

```
    {
        "global": {
            "check_for_updates_on_startup": true,
            "show_in_menu_bar": true,
            "show_profile_name_in_menu_bar": false
        },
        "profiles": [
            {
                "complex_modifications": {
                    "parameters": {
                        "basic.simultaneous_threshold_milliseconds": 50,
                        "basic.to_delayed_action_delay_milliseconds": 500,
                        "basic.to_if_alone_timeout_milliseconds": 1000,
                        "basic.to_if_held_down_threshold_milliseconds": 500,
                        "mouse_motion_to_scroll.speed": 100
                    },
                    "rules": [
                        {
                            "manipulators": [
                                {
                                    "description": "Change right_option to commandcontroloptionshift.",
                                    "from": {
                                        "key_code": "right_option",
                                        "modifiers": {
                                            "optional": [
                                                "any"
                                            ]
                                        }
                                    },
                                    "to": [
                                        {
                                            "key_code": "left_shift",
                                            "modifiers": [
                                                "left_command",
                                                "left_control",
                                                "left_option"
                                            ]
                                        }
                                    ],
                                    "type": "basic"
                                }
                            ]
                        }
                    ]
                },
                "devices": [
                    {
                        "disable_built_in_keyboard_if_exists": false,
                        "fn_function_keys": [],
                        "identifiers": {
                            "is_keyboard": true,
                            "is_pointing_device": false,
                            "product_id": 67,
                            "vendor_id": 5426
                        },
                        "ignore": false,
                        "manipulate_caps_lock_led": false,
                        "simple_modifications": []
                    },
                    {
                        "disable_built_in_keyboard_if_exists": false,
                        "fn_function_keys": [],
                        "identifiers": {
                            "is_keyboard": false,
                            "is_pointing_device": true,
                            "product_id": 67,
                            "vendor_id": 5426
                        },
                        "ignore": true,
                        "manipulate_caps_lock_led": false,
                        "simple_modifications": []
                    },
                    {
                        "disable_built_in_keyboard_if_exists": false,
                        "fn_function_keys": [],
                        "identifiers": {
                            "is_keyboard": true,
                            "is_pointing_device": false,
                            "product_id": 591,
                            "vendor_id": 1452
                        },
                        "ignore": false,
                        "manipulate_caps_lock_led": true,
                        "simple_modifications": []
                    },
                    {
                        "disable_built_in_keyboard_if_exists": false,
                        "fn_function_keys": [
                            {
                                "from": {
                                    "key_code": "f1"
                                },
                                "to": {
                                    "consumer_key_code": "display_brightness_decrement"
                                }
                            },
                            {
                                "from": {
                                    "key_code": "f2"
                                },
                                "to": {
                                    "consumer_key_code": "display_brightness_increment"
                                }
                            },
                            {
                                "from": {
                                    "key_code": "f3"
                                },
                                "to": {
                                    "key_code": "mission_control"
                                }
                            },
                            {
                                "from": {
                                    "key_code": "f4"
                                },
                                "to": {
                                    "key_code": "launchpad"
                                }
                            },
                            {
                                "from": {
                                    "key_code": "f5"
                                },
                                "to": {
                                    "consumer_key_code": "rewind"
                                }
                            },
                            {
                                "from": {
                                    "key_code": "f6"
                                },
                                "to": {
                                    "consumer_key_code": "play_or_pause"
                                }
                            },
                            {
                                "from": {
                                    "key_code": "f7"
                                },
                                "to": {
                                    "consumer_key_code": "fastforward"
                                }
                            },
                            {
                                "from": {
                                    "key_code": "f8"
                                },
                                "to": {
                                    "consumer_key_code": "mute"
                                }
                            },
                            {
                                "from": {
                                    "key_code": "f9"
                                },
                                "to": {
                                    "consumer_key_code": "volume_decrement"
                                }
                            },
                            {
                                "from": {
                                    "key_code": "f10"
                                },
                                "to": {
                                    "consumer_key_code": "volume_increment"
                                }
                            },
                            {
                                "from": {
                                    "key_code": "f11"
                                },
                                "to": {
                                    "key_code": "f11"
                                }
                            },
                            {
                                "from": {
                                    "key_code": "f12"
                                },
                                "to": {
                                    "key_code": "f12"
                                }
                            }
                        ],
                        "identifiers": {
                            "is_keyboard": true,
                            "is_pointing_device": false,
                            "product_id": 34050,
                            "vendor_id": 2652
                        },
                        "ignore": false,
                        "manipulate_caps_lock_led": false,
                        "simple_modifications": []
                    },
                    {
                        "disable_built_in_keyboard_if_exists": false,
                        "fn_function_keys": [],
                        "identifiers": {
                            "is_keyboard": true,
                            "is_pointing_device": false,
                            "product_id": 615,
                            "vendor_id": 76
                        },
                        "ignore": false,
                        "manipulate_caps_lock_led": true,
                        "simple_modifications": []
                    }
                ],
                "fn_function_keys": [
                    {
                        "from": {
                            "key_code": "f1"
                        },
                        "to": {
                            "consumer_key_code": "display_brightness_decrement"
                        }
                    },
                    {
                        "from": {
                            "key_code": "f2"
                        },
                        "to": {
                            "consumer_key_code": "display_brightness_increment"
                        }
                    },
                    {
                        "from": {
                            "key_code": "f3"
                        },
                        "to": {
                            "key_code": "mission_control"
                        }
                    },
                    {
                        "from": {
                            "key_code": "f4"
                        },
                        "to": {
                            "key_code": "launchpad"
                        }
                    },
                    {
                        "from": {
                            "key_code": "f5"
                        },
                        "to": {
                            "key_code": "illumination_decrement"
                        }
                    },
                    {
                        "from": {
                            "key_code": "f6"
                        },
                        "to": {
                            "key_code": "illumination_increment"
                        }
                    },
                    {
                        "from": {
                            "key_code": "f7"
                        },
                        "to": {
                            "consumer_key_code": "rewind"
                        }
                    },
                    {
                        "from": {
                            "key_code": "f8"
                        },
                        "to": {
                            "consumer_key_code": "play_or_pause"
                        }
                    },
                    {
                        "from": {
                            "key_code": "f9"
                        },
                        "to": {
                            "consumer_key_code": "fastforward"
                        }
                    },
                    {
                        "from": {
                            "key_code": "f10"
                        },
                        "to": {
                            "consumer_key_code": "mute"
                        }
                    },
                    {
                        "from": {
                            "key_code": "f11"
                        },
                        "to": {
                            "consumer_key_code": "volume_decrement"
                        }
                    },
                    {
                        "from": {
                            "key_code": "f12"
                        },
                        "to": {
                            "consumer_key_code": "volume_increment"
                        }
                    }
                ],
                "name": "Default profile",
                "parameters": {
                    "delay_milliseconds_before_open_device": 1000
                },
                "selected": true,
                "simple_modifications": [
                    {
                        "from": {
                            "consumer_key_code": "eject"
                        },
                        "to": {
                            "key_code": "f19"
                        }
                    },
                    {
                        "from": {
                            "key_code": "caps_lock"
                        },
                        "to": {
                            "key_code": "f20"
                        }
                    },
                    {
                        "from": {
                            "key_code": "delete_forward"
                        },
                        "to": {
                            "key_code": "fn"
                        }
                    }
                ],
                "virtual_hid_keyboard": {
                    "country_code": 0,
                    "mouse_key_xy_scale": 100
                }
            },
            {
                "complex_modifications": {
                    "parameters": {
                        "basic.simultaneous_threshold_milliseconds": 50,
                        "basic.to_delayed_action_delay_milliseconds": 500,
                        "basic.to_if_alone_timeout_milliseconds": 1000,
                        "basic.to_if_held_down_threshold_milliseconds": 500,
                        "mouse_motion_to_scroll.speed": 100
                    },
                    "rules": [
                        {
                            "manipulators": [
                                {
                                    "description": "Change right_option to commandcontroloptionshift.",
                                    "from": {
                                        "key_code": "right_option",
                                        "modifiers": {
                                            "optional": [
                                                "any"
                                            ]
                                        }
                                    },
                                    "to": [
                                        {
                                            "key_code": "left_shift",
                                            "modifiers": [
                                                "left_command",
                                                "left_control",
                                                "left_option"
                                            ]
                                        }
                                    ],
                                    "type": "basic"
                                }
                            ]
                        }
                    ]
                },
                "devices": [
                    {
                        "disable_built_in_keyboard_if_exists": false,
                        "fn_function_keys": [],
                        "identifiers": {
                            "is_keyboard": true,
                            "is_pointing_device": false,
                            "product_id": 591,
                            "vendor_id": 1452
                        },
                        "ignore": false,
                        "manipulate_caps_lock_led": true,
                        "simple_modifications": []
                    },
                    {
                        "disable_built_in_keyboard_if_exists": false,
                        "fn_function_keys": [
                            {
                                "from": {
                                    "key_code": "f1"
                                },
                                "to": {
                                    "consumer_key_code": "display_brightness_decrement"
                                }
                            },
                            {
                                "from": {
                                    "key_code": "f2"
                                },
                                "to": {
                                    "consumer_key_code": "display_brightness_increment"
                                }
                            },
                            {
                                "from": {
                                    "key_code": "f3"
                                },
                                "to": {
                                    "key_code": "mission_control"
                                }
                            },
                            {
                                "from": {
                                    "key_code": "f4"
                                },
                                "to": {
                                    "key_code": "launchpad"
                                }
                            },
                            {
                                "from": {
                                    "key_code": "f5"
                                },
                                "to": {
                                    "consumer_key_code": "rewind"
                                }
                            },
                            {
                                "from": {
                                    "key_code": "f6"
                                },
                                "to": {
                                    "consumer_key_code": "play_or_pause"
                                }
                            },
                            {
                                "from": {
                                    "key_code": "f7"
                                },
                                "to": {
                                    "consumer_key_code": "fastforward"
                                }
                            },
                            {
                                "from": {
                                    "key_code": "f8"
                                },
                                "to": {
                                    "consumer_key_code": "mute"
                                }
                            },
                            {
                                "from": {
                                    "key_code": "f9"
                                },
                                "to": {
                                    "consumer_key_code": "volume_decrement"
                                }
                            },
                            {
                                "from": {
                                    "key_code": "f10"
                                },
                                "to": {
                                    "consumer_key_code": "volume_increment"
                                }
                            },
                            {
                                "from": {
                                    "key_code": "f11"
                                },
                                "to": {
                                    "key_code": "f11"
                                }
                            },
                            {
                                "from": {
                                    "key_code": "f12"
                                },
                                "to": {
                                    "key_code": "f12"
                                }
                            }
                        ],
                        "identifiers": {
                            "is_keyboard": true,
                            "is_pointing_device": false,
                            "product_id": 34050,
                            "vendor_id": 2652
                        },
                        "ignore": false,
                        "manipulate_caps_lock_led": false,
                        "simple_modifications": []
                    }
                ],
                "fn_function_keys": [
                    {
                        "from": {
                            "key_code": "f1"
                        },
                        "to": {
                            "consumer_key_code": "display_brightness_decrement"
                        }
                    },
                    {
                        "from": {
                            "key_code": "f2"
                        },
                        "to": {
                            "consumer_key_code": "display_brightness_increment"
                        }
                    },
                    {
                        "from": {
                            "key_code": "f3"
                        },
                        "to": {
                            "key_code": "mission_control"
                        }
                    },
                    {
                        "from": {
                            "key_code": "f4"
                        },
                        "to": {
                            "key_code": "launchpad"
                        }
                    },
                    {
                        "from": {
                            "key_code": "f5"
                        },
                        "to": {
                            "key_code": "illumination_decrement"
                        }
                    },
                    {
                        "from": {
                            "key_code": "f6"
                        },
                        "to": {
                            "key_code": "illumination_increment"
                        }
                    },
                    {
                        "from": {
                            "key_code": "f7"
                        },
                        "to": {
                            "consumer_key_code": "rewind"
                        }
                    },
                    {
                        "from": {
                            "key_code": "f8"
                        },
                        "to": {
                            "consumer_key_code": "play_or_pause"
                        }
                    },
                    {
                        "from": {
                            "key_code": "f9"
                        },
                        "to": {
                            "consumer_key_code": "fastforward"
                        }
                    },
                    {
                        "from": {
                            "key_code": "f10"
                        },
                        "to": {
                            "consumer_key_code": "mute"
                        }
                    },
                    {
                        "from": {
                            "key_code": "f11"
                        },
                        "to": {
                            "consumer_key_code": "volume_decrement"
                        }
                    },
                    {
                        "from": {
                            "key_code": "f12"
                        },
                        "to": {
                            "consumer_key_code": "volume_increment"
                        }
                    }
                ],
                "name": "Grego",
                "parameters": {
                    "delay_milliseconds_before_open_device": 1000
                },
                "selected": false,
                "simple_modifications": [
                    {
                        "from": {
                            "key_code": "caps_lock"
                        },
                        "to": {
                            "key_code": "f20"
                        }
                    },
                    {
                        "from": {
                            "key_code": "delete_forward"
                        },
                        "to": {
                            "key_code": "fn"
                        }
                    },
                    {
                        "from": {
                            "key_code": "q"
                        },
                        "to": {
                            "key_code": "u"
                        }
                    },
                    {
                        "from": {
                            "key_code": "u"
                        },
                        "to": {
                            "key_code": "y"
                        }
                    },
                    {
                        "from": {
                            "key_code": "y"
                        },
                        "to": {
                            "key_code": "q"
                        }
                    }
                ],
                "virtual_hid_keyboard": {
                    "country_code": 0,
                    "mouse_key_xy_scale": 100
                }
            },
            {
                "complex_modifications": {
                    "parameters": {
                        "basic.simultaneous_threshold_milliseconds": 50,
                        "basic.to_delayed_action_delay_milliseconds": 500,
                        "basic.to_if_alone_timeout_milliseconds": 1000,
                        "basic.to_if_held_down_threshold_milliseconds": 500,
                        "mouse_motion_to_scroll.speed": 100
                    },
                    "rules": []
                },
                "devices": [
                    {
                        "disable_built_in_keyboard_if_exists": false,
                        "fn_function_keys": [
                            {
                                "from": {
                                    "key_code": "f1"
                                },
                                "to": {
                                    "key_code": "f1"
                                }
                            },
                            {
                                "from": {
                                    "key_code": "f2"
                                },
                                "to": {
                                    "key_code": "f2"
                                }
                            }
                        ],
                        "identifiers": {
                            "is_keyboard": true,
                            "is_pointing_device": false,
                            "product_id": 34050,
                            "vendor_id": 2652
                        },
                        "ignore": false,
                        "manipulate_caps_lock_led": false,
                        "simple_modifications": []
                    }
                ],
                "fn_function_keys": [
                    {
                        "from": {
                            "key_code": "f1"
                        },
                        "to": {
                            "key_code": "f1"
                        }
                    },
                    {
                        "from": {
                            "key_code": "f2"
                        },
                        "to": {
                            "consumer_key_code": "display_brightness_increment"
                        }
                    },
                    {
                        "from": {
                            "key_code": "f3"
                        },
                        "to": {
                            "key_code": "mission_control"
                        }
                    },
                    {
                        "from": {
                            "key_code": "f4"
                        },
                        "to": {
                            "key_code": "launchpad"
                        }
                    },
                    {
                        "from": {
                            "key_code": "f5"
                        },
                        "to": {
                            "key_code": "illumination_decrement"
                        }
                    },
                    {
                        "from": {
                            "key_code": "f6"
                        },
                        "to": {
                            "key_code": "illumination_increment"
                        }
                    },
                    {
                        "from": {
                            "key_code": "f7"
                        },
                        "to": {
                            "consumer_key_code": "rewind"
                        }
                    },
                    {
                        "from": {
                            "key_code": "f8"
                        },
                        "to": {
                            "consumer_key_code": "play_or_pause"
                        }
                    },
                    {
                        "from": {
                            "key_code": "f9"
                        },
                        "to": {
                            "consumer_key_code": "fastforward"
                        }
                    },
                    {
                        "from": {
                            "key_code": "f10"
                        },
                        "to": {
                            "consumer_key_code": "mute"
                        }
                    },
                    {
                        "from": {
                            "key_code": "f11"
                        },
                        "to": {
                            "consumer_key_code": "volume_decrement"
                        }
                    },
                    {
                        "from": {
                            "key_code": "f12"
                        },
                        "to": {
                            "consumer_key_code": "volume_increment"
                        }
                    }
                ],
                "name": "Kinesis",
                "parameters": {
                    "delay_milliseconds_before_open_device": 1000
                },
                "selected": false,
                "simple_modifications": [],
                "virtual_hid_keyboard": {
                    "country_code": 0,
                    "mouse_key_xy_scale": 100
                }
            }
        ]
    }

```