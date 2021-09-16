<script>
    import { createForm } from 'svelte-forms-lib';

    const { form, handleSubmit, handleChange } = createForm({
        initialValues: { a: 1 },
        onSubmit: values => {
            alert(JSON.stringify(values));
        },
    });
</script>

<form on:submit={handleSubmit}>
    <select name="a" value={$form.a} on:change={handleChange}>
        <option />
        <option value={0}>Foo</option>
        <option value={1}>Bar</option>
        <option value={2}>Baz</option>
    </select>
    <button type="submit">submit</button>
</form>
