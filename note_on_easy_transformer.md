It would be nice to have a documentation on the hook (how to create one, ...)

Function idea

```python
def layername(num=0, _type=None):
    # Layer translation for top level hooks on EasyTranformer
    supported_hooks = ["embed", "pos_embed", "resid_pre", "resid_mid", "resid_post", "attn_out", "mlp_out"]
    assert _type in supported_hooks, f"type must be one of {supported_hooks}"
    
    if _type == "embed":
        return "hook_embed"
    
    if _type == "pos_embed":
        return "hook_pos_embed"

    return f"blocks.{num}.hook_{_type}"
```
