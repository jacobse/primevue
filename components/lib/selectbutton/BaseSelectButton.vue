<script>
import BaseComponent from 'primevue/basecomponent';
import SelectButtonStyle from 'primevue/selectbutton/style';

export default {
    name: 'BaseSelectButton',
    extends: BaseComponent,
    props: {
        modelValue: null,
        options: Array,
        optionLabel: null,
        optionValue: null,
        optionDisabled: null,
        multiple: Boolean,
        unselectable: {
            type: Boolean,
            default: true
        },
        allowEmpty: {
            type: Boolean,
            default: true
        },
        disabled: Boolean,
        dataKey: null,
        'aria-labelledby': {
            type: String,
            default: null
        }
    },
    style: SelectButtonStyle,
    provide() {
        return {
            $parentInstance: this
        };
    }
};
</script>
